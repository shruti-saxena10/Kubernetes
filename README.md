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

APP1      APP2
8GB       20GB
Worker Nodes
15GB   25GB
Master Node will decide on which worker node app will be deployed

Corporate specifications
Worker node->32GB of RAM 150GB of storage

CLUSTER ARCHITECTURE

<img width="810" alt="Screenshot 2024-05-30 at 4 18 33 PM" src="https://github.com/shruti-saxena10/Kubernetes/assets/108339410/e1a66234-7d91-4236-a42b-6a9cc5855fec">



Master Node(Control Plane)
1.API Server->Cluster gateway->Requests(Deploy-Upgrade-Scale up the pod) goes to it.

2.ETCD->called as cluster brain->stores the information about cluster configration, whichever pod is being created and which application is being deployed and stores in the form of key-value pairs .
key :  Value
name: Shruti

3.SCHEDULER->Resposible for assigning a worker node on which the newly request that came is going to be created on based of availability and requirement
eg :-The pod requires 30-40GB of RAM
and scheduller will see if which worker node has that much RAM and is available.Pod will assigned to that and pod will be created on that worker node.

