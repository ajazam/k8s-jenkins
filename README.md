# k8s-jenkins
Instructions to install jenkins in Kubernetes with persistent storage on NFS

The yaml file makes use of an ingress object. The load balancer used in my setup is [Traefik](https://traefik.io)

To install jenkins download this repo and use kubectl
>kubectl create -f complete.yaml