# Workshop :: Docker Swarm
* NodeJS

## Step to run

### 1. Create cluster
```
$docker swarm init
$docker node ls
```

### 2. Build image
```
$docker compose build
```

### 3. Deploy to Docker swarm cluster
```
$docker stack deploy --compose-file docker-compose-deploy.yml demo

$docker service ls
ID             NAME       MODE         REPLICAS   IMAGE                       PORTS
xv1xgf3sgby2   demo_api   replicated   1/1        somkiat/demo-nodejs:1.0.0   *:3000->3000/tcp
```

Access to http://localhost:3000
```
curl http://localhost:3000/
```

### 4. Scale service
```
$docker service scale demo_api=5
$docker service ls
```

### Leave from cluster
```
docker swarm leave -f
```
