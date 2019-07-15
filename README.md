# Burek Frontend

```bash
docker build -t itspektar/burek-frontend:latest .
docker-compose up -d
# docker stack deploy -c docker-compose.yaml burek-frontend
curl localhost:50080 # or open in browser
You should see in the content a sentence:
Hello World! I have been seen 1 times.
```

