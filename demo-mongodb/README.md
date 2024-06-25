# Setup mongodb cluster

```
docker compose up --wait
docker compose ps
```

### Access to MongoDB Admin
* http://localhost:8081/
  * user=admin
  * password=pass

### Access to server
```
docker exec -it mongo1 bash

>mongosh
>rs.status()
```