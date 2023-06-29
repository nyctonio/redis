# Host your self managed redis instance.

```
docker build -t <your username>/redis .
eg -> docker build -t nio/redis .

run the docker file using
docker run --name redis -p 6379:6379 -d nio/redis

install redis-cli to interact internally
```

## Create ACL Users for the redis

```
connect to the redis

docker exec -it redis redis-cli

ACL LIST - this will list all the users
ACL SETUSER <username> on ><password> ~* &* +@all      -- create new user

```
