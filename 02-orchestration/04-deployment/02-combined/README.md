# Deploy an App from a Single File

This app.yml file shows how you can combine a _service_ and _deployment_ into a single file.

```bash

# Use kubectl to create the namespace
kubectl apply -f app.yml -n learn-aks

kubectl get all --all-namespaces

# Clean up
kubectl delete namespace learn-aks
```