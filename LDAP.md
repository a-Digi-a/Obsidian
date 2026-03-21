#computing 

# LDAP

## Installing openldap

```shell
sudo apt-update
sudo apt-install slapd ldap-utils
cd
mkdir ldap
cd ldap
sudo dpkg-reconfigure -plow slapd
```

a ui will pop up, this will let you set up the cn and organisation

### Check if it works

```shell
ldapsearch -x -LLL -s base -b "" namingContexts
```

