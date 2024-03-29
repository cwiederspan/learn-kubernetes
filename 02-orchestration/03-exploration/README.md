# Explore Your Kubernetes Cluster

```bash

# Get your credentials from AKS
az aks get-credentials -g $RG_NAME -n $RG_NAME

# Now you can use kubectl
kubectl describe nodes | grep -e "Name:" -e "failure-domain.beta.kubernetes.io/zone"

# Show the namespaces
kubectl get namespaces

# Show all pods in all namespaces
kubectl get pods --all-namespaces

# Filter by a namespace
kubectl get pods -n kube-system

# Show all services in all namespaces
kubectl get services --all-namespaces

# Show all deployments in all namespaces
kubectl get deployments --all-namespaces

# Describe some things
kubectl describe pod nginx-ingress-controller -n ingress-basic

kubectl describe service kube-dns -n kube-system

```
