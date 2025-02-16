## Guideline

1. Run Docker Desktop.
2. Create a Kind cluster:
   ```
   kind create cluster --config kind-config.yaml
   ```
3. Deploy Redis:
   ```
   kubectl apply -f redis-deployment.yaml
   kubectl apply -f redis-service.yaml
   ```
4. Access Redis:
   ```
   kubectl port-forward svc/redis 6379:6379
   redis-cli -h 127.0.0.1 -p 6379
   ```

## Testing Redis

Connect to Redis using `redis-cli`:
   ```bash
   redis-cli -h 127.0.0.1 -p 6379
   ```
Set and Get a key:
   ```
   SET mykey "Hello, Redis!"
   GET mykey
   ```

   
