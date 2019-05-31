# Setup Helm on the Cluster

Helm is the defacto standard for package management and deployment on Kubernetes.

<https://helm.sh/>

```bash

# Setup the RBAC prerequisites
kubectl create -f helm-rbac.yml

# Initialize Helm on the cluster
helm init --service-account tiller

```