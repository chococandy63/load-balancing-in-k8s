# load-balancing-in-k8s
Creating A Load Balancer using kubernetes

## Kubernetes Architecture 

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/f2d7da6c-f15d-4429-a922-4d39dfee0894)


### Why Load Balancing is required?




### Real-life examples of load balancing used in production environments



## Load Balancing in K8s


### Kubernetes Cluster Setup

Install minikube, kubectl on your system.

Minikube is used to create a local K8s cluster. After installing minikube, run the following commands to start a minikube cluster on docker.

- Create a Kubernetes cluster: You need to have a Kubernetes cluster running on Fedora. You can use a tool like kubeadm to create a cluster.
- Create a deployment: You need to create a deployment that defines the pods that will run your application. You can use a YAML file to define the deployment.
- Create a service: You need to create a service that exposes your deployment to the network. You can use a YAML file to define the service. In the YAML file, you can specify the type field as LoadBalancer to create a load balancer service.
- Deploy the service: You can deploy the service using the kubectl create command.

Step 1: `minikube start --driver=kvm2`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/9c869cb2-00f3-4699-9429-2321303ba968)


It will perform the following tasks:
- Starting control plane node minikube in cluster minikube
- Pulling base image ...
    > gcr.io/k8s-minikube/kicbase..
- Preparing Kubernetes v1.28.3 on kvm.
- kubectl is now configured to use "minikube" cluster and "default" namespace by default

Reference: [https://minikube.sigs.k8s.io/docs/drivers/kvm2/](https://minikube.sigs.k8s.io/docs/drivers/kvm2/)

Step 2: Deployment of minikube(kubernetes cluster)

`kubectl apply -f deployment.yaml`

You should get an output similar to this:

        service/flask-test-service created
        deployment.apps/flask-test-app created

Step 3: 

`kubectl get po -A`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/fcdd1ebd-b1eb-4dee-b318-a273d734396c)

`kubectl get po`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/36270008-ce40-4b1e-8ad2-135a3d3b2a80)


`kubectl get svc`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/8bd120df-1a10-4f8e-9159-c010a227649f)

`minikube dashboard`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/23136488-9549-430a-90d0-aee294faeb64)


On the browser, 

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/3d264138-b94a-4ee6-95f7-a1e8123eb65d)

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/16006291-ae24-433f-b665-1f4bbc840885)

You can access your flask application in your local host browser. 

`minikube service flask-test-service`

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/615c62bc-4351-4886-9c8d-c4cafc071d6c)

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/1f779b43-755a-4050-be9c-46302215cdac)






Reference: [https://minikube.sigs.k8s.io/docs/start/](https://minikube.sigs.k8s.io/docs/start/)
[https://minikube.sigs.k8s.io/docs/drivers/kvm2/](https://minikube.sigs.k8s.io/docs/drivers/kvm2/)


Docker Hub

![image](https://github.com/chococandy63/load-balancing-in-k8s/assets/79960426/7a674a09-49f5-4da7-979c-d38739d02ea1)





