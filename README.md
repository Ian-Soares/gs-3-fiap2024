# gs-3-fiap2024

## Running commands
- Compose
```
docker compose up
```
- Express example hello world app
```
cd app
docker build --no-cache -t node-test .
docker container run --rm --name node-test-container -p 9090:8090 node-test:latest
```
- Nginx example index.html page
```
cd nginx
docker build --no-cache -t nginx-test .
docker container run --rm --name nginx-test-container -p 8080:80 nginx-test:latest
```