# Kubernetes Ingress

## Install an Ingress Controller

```bash

# Create a namespace for your ingress resources
kubectl create namespace ingress-basic

# Use Helm to deploy an NGINX ingress controller
helm install stable/nginx-ingress \
    --namespace ingress-basic \
    --set controller.replicaCount=2 \
    --set controller.nodeSelector."beta\.kubernetes\.io/os"=linux \
    --set defaultBackend.nodeSelector."beta\.kubernetes\.io/os"=linux
```

## Install an App with Ingress

```bash

# Use kubectl to create the namespace
kubectl apply -f ingress.yaml -n learn-aks

# List all of the ingresses
kubectl get ingress --all-namespaces

# Describe the ingress we just created
kubectl describe ingress basic-ingress -n learn-aks

```