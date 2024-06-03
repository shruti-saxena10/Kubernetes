# Kubernetes
Advantages of kubernetes
1.OpenSource

2.Manages container(Container Orchestration tool)

3.Automate deployment

4.Autohealing 

Architecture
node->VM
Two kinds of node->master and worker node(depends on how we configure tools)
Master is going to manage the worker nodes(multiple)

APP1->8GB      APP2->20GB
       
Worker Nodes->15GB   25GB
Master Node will decide on which worker node app will be deployed

Corporate specifications
Worker node->32GB of RAM 150GB of storage

CLUSTER ARCHITECTURE

<img width="810" alt="Screenshot 2024-05-30 at 4 18 33 PM" src="https://github.com/shruti-saxena10/Kubernetes/assets/108339410/e1a66234-7d91-4236-a42b-6a9cc5855fec">



Cluster Architecture

Master Node(Control Plane)
1.Kube API Server->Cluster gateway->Requests(Deploy-Upgrade-Scale up the pod) goes to it.


2.ETCD->called as cluster brain->stores the information about cluster configration, whichever pod is being created and which application is being deployed and stores in the form of key-value pairs .
key :  Value
name: Shruti

3.SCHEDULER->Resposible for assigning a worker node on which the newly request that came is going to be created on based of availability and requirement
eg :-The pod requires 30-40GB of RAM
and scheduller will see if which worker node has that much RAM and is available.Pod will assigned to that and pod will be created on that worker node.


4.CONTROLLER Manager->Detect the state changes in pod.
eg:-We have deployed our application and pod is running.For some reason, the pod got destroyed,removed or stopped or scaled down.those changes are detected by the controller manager and it will inform scheduller that it should be up.

5.Cloud-controller manager
A Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.

Worker Node-1(Date Plane)
1.Kublet-->Responsible for Creation of pod or resources with respect to applications

2.Containerruntime-->Manages the containers

3.Kube-Proxy-->Responsible for Networking inside our cluster
Worker Node-2Date Plane)
1.Kublet

2.Containerruntime

3.Kube-Proxy


Basic Architecture of application with components
<img width="1194" alt="Screenshot 2024-05-31 at 11 45 33 AM" src="https://github.com/shruti-saxena10/Kubernetes/assets/108339410/484fc3ba-b246-4e40-b797-e20d20a1a997">


Components 

Pod 

Service

Scerets

ConfigMap

PVC

PV


<img width="1448" alt="Screenshot 2024-06-03 at 10 56 29 AM" src="https://github.com/shruti-saxena10/Kubernetes/assets/108339410/12a72100-d5c9-4d0f-adba-dc6df6b4f021">






