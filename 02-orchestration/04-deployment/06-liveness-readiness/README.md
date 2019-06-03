# Liveness and Readiness for Zero Downtime Deployments

## Liveness

A configurable probe that determines whether or not a running container is healthy. This is used to determine if/when
a workload should be restarted.

## Readiness

A configurable probe used by the control plane to determine whether or not to send traffic to a container. This useful
when starting up a container.

## Useful for Zero Downtime Deployments

When deploying new or updating existing apps in Kubernetes, the liveness and readiness probes allow you to ensure zero 
downtime deployments.

[Brendan Burns explains zero downtime deployments](https://youtu.be/mNK14yXIZF4)