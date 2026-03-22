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
nvim users.ldif
```

inside **users.ldif**:
```txt

```