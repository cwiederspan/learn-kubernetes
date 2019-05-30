# Introduction to Kubernetes

## Resources

* [Children's Guide to Kubernetes](https://www.cncf.io/wp-content/uploads/2019/03/The-Illustrated-Childrens-Guide-to-Kubernetes.pdf)

* [Phippy Goes to the Zoo](https://azure.microsoft.com/mediahandler/files/resourcefiles/phippy-goes-to-the-zoo/Phippy%20Goes%20To%20The%20Zoo_MSFTonline.pdf)

* [Kubernetes in 50 Days](https://azure.microsoft.com/mediahandler/files/resourcefiles/kubernetes-learning-path/Kubernetes%20Learning%20Path%20version%201.0.pdf)

## Glossary

* **etcd** - Consistent and highly-available key value store used as Kubernetes’ backing store for all cluster data.

<!-- * **Controller** - A daemon that embeds the core control loops shipped with Kubernetes. In applications of robotics and automation, a control loop is a non-terminating loop that regulates the state of the system. In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the API server and makes changes attempting to move the current state towards the desired state. Examples of controllers that ship with Kubernetes today are the replication controller, endpoints controller, namespace controller, and service accounts controller. -->

* **Namespace** - Allows partitioning of a physical cluster into multiple virtual clusters.

<!-- * **Name** - All objects in the Kubernetes are unambiguously identified by a Name. -->

* **Pod** - The basic building block of Kubernetes. Pods are responsible for running your containers. Every Pod holds at least one container, and controls the execution of that container. When the containers exit, the Pod dies too.

* **Deployment** - A higher-order abstraction that controls deploying and maintaining a set of Pods. Behind the scenes, it uses a ReplicaSet to keep the Pods running, but it offers sophisticated logic for deploying, updating, and scaling a set of Pods within a cluster.

* **Service** - An abstraction which defines a logical set of Pods and a policy by which to access them. While pods come and go, the service IP addresses and ports remain the same. Other applications can find your service through Kubernetes service discovery.

* **Ingress** - Provide a way to declare that traffic ought to be channeled from the outside of the cluster into destination points within the cluster. One single external Ingress point can accept traffic destined to many different internal services.

* **ReplicaSet** - A ReplicaSet ensures that a set of identically configured Pods are running at the desired replica count. If a Pod drops off, the ReplicaSet brings a new one online as a replacement.

* **Secret** - Used to store non-public information, such as tokens, certificates, or passwords. Secrets can be attached to Pods at runtime so that sensitive configuration data can be stored securely in the cluster.

* **DaemonSets** - Provide a way to ensure that a copy of a Pod is running on every node in the cluster. As a cluster grows and shrinks, the DaemonSet spreads these specially labeled Pods across all of the nodes.