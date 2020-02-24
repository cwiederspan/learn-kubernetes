# Coupling Pods to Nodes

Determining which nodes you want your workloads to run on can be useful in certain situations:

* OS (Linux vs. Windows)
* Hardware Specs (GPU)
* Availability Zones

## Node Selector

This is the easiest way to ensure that a pod runs on a certain type of node. In this context, we are _attacting_ pods to certain nodes.

<https://kubernetes.io/docs/concepts/configuration/assign-pod-node/#nodeselector>

## Node Affinity (Beta)

Like Node Selector functionality, this beta feature allows you to target nodes for pods to run on. It provides
more powerful syntax and functionality, but is currently in beta.

<https://kubernetes.io/docs/concepts/configuration/assign-pod-node/#node-affinity-beta-feature>

## Taints and Tolerations

Taints and tolerations work together to ensure that pods are not scheduled onto inappropriate nodes. In this context, we
are _repelling_ pods from certain nodes.

* You **Taint** a node with a certain set of attributes
* Your pod can then **Tolerate** being put on those tainted nodes

> One interesting use case for taints is the ability to taint a node which will ultimately cause the eviction 
> of all workloads on that node. This might be useful for performing maintenance on that node, or when the node 
> has problems and you want force the workloads to other nodes.
