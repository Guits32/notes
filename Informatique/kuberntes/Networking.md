## Purpose of kube-proxy and CNI plugins

For details, check this [article](https://medium.com/@seifeddinerajhi/kube-proxy-and-cni-the-hidden-components-of-kubernetes-networking-eb30000bf87a#:~:text=Kubernetes%20networking%20is%20powered%20by,running%20containerized%20applications%20on%20Kubernetes).

As an overview:
- CNI plugin is responsible of managing the inside kube network. It is responsible to allow IP (by working with  the IP Adress Management - IPAM) to each container. It is also responsible of deleting IP allocation of dead/stopped containers.
- kube-proxy is responsible to map static IP to 