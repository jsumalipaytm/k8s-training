

```
kubectl apply -f redis-master-deployment.yaml

kubectl apply -f redis-master-service.yaml

kubectl apply -f redis-slave-deployment.yaml

kubectl apply -f redis-slave-service.yaml

kubectl apply -f frontend-deployment.yaml

kubectl apply -f frontend-service.yaml
```


kubectl set image deployments/frontend php-redis=gcr.io/google-samples/gb-frontend:v6

kubectl rollout status deployments/frontend

