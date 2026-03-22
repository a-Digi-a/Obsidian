#computing 

# LDAP

## Installing openldap

```shell
sudo apt-update
sudo apt-install slapd ldap-utils
sudo dpkg-reconfigure -plow slapd
```

a ui will pop up, this will let you set up the cn and organisation

### Check if it works

```shell
ldapsearch -x -LLL -s base -b "" namingContexts
```

## Create Organisational units

```shell
cd
mkdir ldap
cd ldap 
nvim ou.ldif
```

inside the file **ou.ldif** (can be named anything):
```ldif
dn: ou=accounts,dc=redbrick,dc=dcu,dc=ie
objectClass: organizationalUnit
ou: accounts

dn: ou=groups,dc=redbrick,dc=dcu,dc=ie
objectClass: organizationalUnit
ou: groups
```

This creates the organisational unit called accounts and another one called groups

now run:
```shell
ldapadd -x -D "cn=admin,dc=redbrick,dc=dcu,dc=ie" -W -f base.ldif
```

This will add the contents of that file to your ldap config

## Adding Users to LDAP


```shell
sudo slappasswd # input the password for your user and save the output (encrypted version)
nvim users.ldif
```

under userPassword use the encrypted password you generated
inside **users.ldif**:
```txt
dn: uid=digi,ou=accounts,dc=redbrick,dc=dcu,dc=ie
objectClass: inetOrgPerson
objectClass: posixAccount
objectClass: top
cn: Digi
sn: Digi
uid: digi
uidNumber: 1001
gidNumber: 1001
homeDirectory: /home/digi
loginShell: /bin/bash
userPassword: {SSHA}H2sXEHWFFsUz7PmvYKHXYxaJ3vfvWoqh

dn: uid=neo,ou=accounts,dc=redbrick,dc=dcu,dc=ie
objectClass: inetOrgPerson
objectClass: posixAccount
objectClass: top
cn: Neo
sn: Neo
uid: neo
uidNumber: 1002
gidNumber: 1002
homeDirectory: /home/neo
loginShell: /bin/bash
userPassword: {SSHA}H2sXEHWFFsUz7PmvYKHXYxaJ3vfvWoqh
```

To test if it worked:
```shell
sudo ldapsearch -x -LLL -b "dc=redbrick,dc=dcu,dc=ie" "(objectClass=posixAccount)"
```

## Deleting Accounts

To delete an account:
```shell
ldapdelete -D "cn=admin,dc=redbrick,dc=dcu,dc=ie" -w a "uid=neo,ou=accounts,dc=redbrick,dc=dcu,dc=ie"
```
change the **uid** to the account you want to delete

## Modify an Entry

first create an ldif file:
```shell
nvim modify.ldif
```

```ldif
dn: uid=neo,ou=accounts,dc=redbrick,dc=dcu,dc=ie
changetype: modify

replace: sn
sn: awa

add: title
title: sysadmin

add: year
year: 3

delete: cn
```

## Add LDAP as an authentication option

```shell
sudo nvim /etc/nsswitch.conf
```

Add ldap to **passwd** and **group**:
```conf
passwd:    files systemd ldap
group:     files systemd ldap
```

Make sure that a new home directory is created for the user:
```txt
sudo nvim /etc/pam.d/common-session
```

Add this line:
```txt
session option pam_mkhomedir.so skel=/etc/skel umask=077
```
