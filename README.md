# load-balancing-in-k8s
Creating A Load Balancer using kubernetes

## Kubernetes Architecture 
[Diagram]

### Why Load Balancing is required?




### Real-life examples of load balancing used in production environments


## Kubernetes Cluster Setup

Install minikube, kubectl on your system.

Minikube is used to create a local K8s cluster. After installing minikube, run the following commands to start a minikube cluster on docker.

Step 1: `minikube start --driver=docker`

It will perform the following tasks:
- Starting control plane node minikube in cluster minikube
- Pulling base image ...
    > gcr.io/k8s-minikube/kicbase..
- It will create a docker container (CPUs=2, Memory=2200MB).
- Preparing Kubernetes v1.28.3 on Docker 24.0.7
- kubectl is now configured to use "minikube" cluster and "default" namespace by default

Reference: [https://minikube.sigs.k8s.io/docs/drivers/docker/](https://minikube.sigs.k8s.io/docs/drivers/docker/)


Step 2: `kubectl get po -A`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/b45602c5-e445-4eb7-ac01-93942256f0fa)

Step 3: `minikube dashboard`


On the browser, 



## LOAD BALANCING IN K8S 

### Steps to demonstrate Load Balancing in Kubernetes

- Setup a Kubernetes deployment using a deployment manifest file: This will create 3 pods replica each with an Nginx image

- Check pods are running or not.

- Create a load balancing service.

- 
