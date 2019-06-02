# Requests and Limits

Setting [Requests and Limits](https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/) is a best practice, especially in environments susceptible to noisy neighbor problems.

> Requests and Limits are applied at the container-level. A pod's request and limit requirements are _calculated_ 
> as sum of the containers running as part of that pod.

<https://github.com/kubernetes/community/blob/master/contributors/design-proposals/node/resource-qos.md>

* CPU => **Compressible**
* Memory => **Incompressible**

## QoS Classes

* Requests == Limits => **Guaranteed** (Highest Priority & Lowest Chance of Eviction)
* Requests < Limits => **Burstable** (Middle of the Road)
* Requests/Limits Not Set => **Best Effort** (Lowest Priority & Highest Chance of Eviction)
