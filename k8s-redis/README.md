## Guideline

1. Run Docker Desktop.
2. Create a Kind cluster:
   ```bash
   kind create cluster --config kind-config.yaml
   ```
3. Deploy Redis:
   ```bash
   kubectl apply -f redis-deployment.yaml
   kubectl apply -f redis-service.yaml
   ```
4. Access Redis:
   ```bash
   kubectl port-forward svc/redis 6379:6379
   redis-cli -h 127.0.0.1 -p 6379
   ```

## Testing Redis

1. Connect to Redis using `redis-cli`:
   ```bash
   redis-cli -h 127.0.0.1 -p 6379
   ```
2. Set a key:
   ```bash
   SET mykey "Hello, Redis!"
   ```
3. Get the key:
   ```bash
   GET mykey
   ```

   
