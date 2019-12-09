# Flask with Mongo and Docker

## Setup

```bash
docker-compose up -d

docker ps
```

```bash
docker exec -it mongodb bash

mongo -u mongodbuser -p
```

```
show dbs;
db.createUser({user: 'flaskuser', pwd: 'your password', roles: [{role: 'readWrite', db: 'flaskdb'}]})
exit
```

```
mongo -u flaskuser -p your password --authenticationDatabase flaskdb
exit
```

## Running the Flask To-do App

```bash
curl -i http://your_server_ip


curl -i\
    -H "Content-Type: application/json" \
    -X POST -d '{"todo": "Dockerize Flask application with MongoDB backend"}'\
    http://your_server_ip/todo


# list all
curl -i http://your_server_ip/todo
```
