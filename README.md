# Burek Frontend

```bash
docker build -t itspektar/burek-frontend:latest .
docker-compose up -d
# docker stack deploy -c docker-compose.yaml burek-frontend
curl localhost:50080 # or open in browser
You should see in the content a sentence:
Hello World! I have been seen 1 times.
```

or for kubernetes
```bash
kubectl apply -f redis-deployment.yaml
kubectl apply -f app-service.yaml
kubectl apply -f web-deployment.yaml
kubectl expose -f redis-deployment.yaml --type=LoadBalancer --name=redis
kubectl expose -f app-deployment.yaml --type=LoadBalancer --name=app
kubectl expose -f web-deployment.yaml --type=LoadBalancer --name=web
curl localhost:5000 # for backend or open in browser
curl localhost # for frontend or open in browser
```
or creating one pod that encapsulates all
```bash
kubectl apply -f burek-pod.yaml
kubectl expose pod burek-pod --type=LoadBalancer --name=burek
curl localhost:5000 # for backend or open in browser
curl localhost # for frontend or open in browser
```

