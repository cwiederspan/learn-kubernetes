# Scale the Number of Pods

```bash

# Scale up the number of pods
kubectl scale deployment.v1.apps/basic-deployment --replicas=3 -n learn-aks

# Scale down the number of pods
kubectl scale deployment.v1.apps/basic-deployment --replicas=1 -n learn-aks

```