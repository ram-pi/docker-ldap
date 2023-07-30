# Run

```
docker-compose up -d
ldapsearch -x -b "ou=users,dc=confluent,dc=io" -H ldap://localhost:389 -D CN=admin,dc=confluent,dc=io -w 'admin'
```