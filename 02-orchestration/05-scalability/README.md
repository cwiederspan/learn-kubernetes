# Scaling Kubernetes

## Pod Scaling

### Manual Scaling

The number of pods used for a workload can be scaled to meet demand. The most basic way of scaling the number of pods
is to manually increase the replica count.

```bash

# Scale up the number of pods
kubectl scale deployment.v1.apps/basic-deployment --replicas=3 -n learn-aks

# Scale down the number of pods
kubectl scale deployment.v1.apps/basic-deployment --replicas=1 -n learn-aks

```

### Horizontal Pod Autoscaling (HPA)

<https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/>

<https://docs.microsoft.com/en-us/azure/aks/concepts-scale#horizontal-pod-autoscaler>

## Node Scaling

### Manual Scaling

You can manually scaled the number of nodes in the cluster.

```bash
az aks scale --resource-group MY_RG_NAME --name MY_AKS_NAME --node-count 3
```

### Cluster Autoscaling

> Cluster Autoscaling is currently in **Preview** and uses Virtual Machine Scale Sets (VMSS) as the mechanism for scaling.

<https://docs.microsoft.com/en-us/azure/aks/cluster-autoscaler>

## Virtual Node for Bursting

<https://docs.microsoft.com/en-us/azure/aks/concepts-scale#burst-to-azure-container-instances>
