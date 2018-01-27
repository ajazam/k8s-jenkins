# k8s-jenkins
Instructions to install jenkins in Kubernetes with persistent storage on NFS

The yaml file makes use of an ingress object. The load balancer used in my setup is [Traefik](https://traefik.io)

If you are installing kubernetes via kubeadm and you are also using the firewall on the nodes then you must allow
incoming udp port 8472 traffic on each node, otherwise node to node communication does not work. Port 8472 is used by the overlay network. This was encountered with Flannel and Canal network plugins. It may also be required by other overlay network plugins but has not been tested.

To install jenkins download this repo and use kubectl
>kubectl create -f complete.yaml
