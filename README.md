# load-balancing-in-k8s
Creating A Load Balancer using kubernetes

## Kubernetes Architecture 
[Diagram]

### Why Load Balancing is required?




### Real-life examples of load balancing used in production environments


## Kubernetes Cluster Setup

Install minikube, kubectl on your system.

Minikube is used to create a local K8s cluster. After installing minikube, run the following commands to start a minikube cluster on docker.

- Create a Kubernetes cluster: You need to have a Kubernetes cluster running on Fedora. You can use a tool like kubeadm to create a cluster.
- Create a deployment: You need to create a deployment that defines the pods that will run your application. You can use a YAML file to define the deployment.
- Create a service: You need to create a service that exposes your deployment to the network. You can use a YAML file to define the service. In the YAML file, you can specify the type field as LoadBalancer to create a load balancer service.
- Deploy the service: You can deploy the service using the kubectl create command.

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

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/9966995e-f6ab-4276-9c44-12431afe1a53)

On the browser, 

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/96b51297-ad1a-4088-9cb7-436a57e5ec05)

Step 4: Deploy applications

Reference: [https://minikube.sigs.k8s.io/docs/start/](https://minikube.sigs.k8s.io/docs/start/)


## LOAD BALANCING IN K8S 

### Steps to demonstrate Load Balancing in Kubernetes

- Setup a Kubernetes deployment using a deployment manifest file: This will create 3 pods replica each with an Nginx image

- Check pods are running or not.

- Create a load balancing service.

