# Deploy a Basic App to Kubernetes

```bash

# Use kubectl to create the namespace
kubectl apply -f namespace.yaml

kubectl get namespaces

# Deploy the application itself
kubectl apply -f deployment.yaml -n learn-aks 

kubectl get pods -n learn-aks

# Deploy the service for accessing the app
kubectl apply -f service.yaml -n learn-aks

kubectl get service -n learn-aks

# Clean up
kubectl delete namespace learn-aks
```