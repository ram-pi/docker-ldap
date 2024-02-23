# Run

```
docker-compose up -d
ldapsearch -x -b "ou=users,dc=confluent,dc=io" -H ldap://localhost:389 -D CN=admin,dc=confluent,dc=io -w 'admin'
ldapsearch -s sub -b "dc=confluent,dc=io" -H ldap://localhost:389 -D CN=admin,dc=confluent,dc=io -w 'admin' "(objectclass=person)" cn memberof
ldapsearch -s sub -b "dc=confluent,dc=io" -H ldap://localhost:389 -D CN=admin,dc=confluent,dc=io -w 'admin' "(objectclass=groupOfNames)" cn member
```