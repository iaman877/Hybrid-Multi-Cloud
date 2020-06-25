# Day18 - Hybrid Multi Cloud 24-06-2020
## Deployment of Multi-Node Kubernetes Cluster with the help of several cloned Virtual Machine. 
* For creating this setup we have installed kubectl on base OS which works as client, one master node and two slave/ worker node on VM.
* When the client try to connect to master then master node will sent the request to slave node and the worker node will provide resources like RAM, CPU. Here we have two slave node, so the master node is using a service called Load Balancer for managing both the node. This cluster is going to manage the container so this is known as Container cluster.

* Kubelet is a program in slave node, when master make a request then this program have to listen to master and have to launch a pod for client.
* Etcd is one of the database service which is used for permanent storage like for secret key which consist of token or username and password.
* Create Kube ApiServer with a name that resolves to DNS and SSH access from one device to all nodes, via use of token from master node. Kube Controller is a program which have works to keep monitoring on pod. Kube Scheduler is a type of service/ program/ daemon which distribute the pod in different slaves.
* K8s doesn't support the cgroup driver 'cgroupfs'. It works properly on 'systemd' cgroup driver. Swap is one type of memory management which we have to disable it.

* Kubeadm is a command which helps to create own multi node K8s cluster. Kubeadm init create a control plane by giving range of IP to pod. Master will create one token and provide to slave so that they can connect.
 
* iproute-tc is used to control network traffic and K8s used this to manage the traffic. Kube-proxy is used to manage the pods to connect to client. We have to create a Flannel network so that two containers can communicate to each other.

* exec bash is a command in rhel8, without logout we can update the hostname.

