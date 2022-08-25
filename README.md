
![](/1_UBwQRP_HpjawvPzlvdHfWw.jpeg)

## MiniKube
* Minikube is a 1 node K8s cluster. It contains both master and worker nodes.
* It is used for testing purposes.  
## Kubectl
* It is a command line tool for k8s cluster.
* It interacts with the cluster by executing different commands on pods like creating, destroying pods
  or creating services.

  

   
## Installation guide

https://minikube.sigs.k8s.io/docs/start/
## CLI commands

* create minikube cluster
   * minikube start
   * kubectl get nodes
   * minikube status
   * kubectl version

* delete cluster and restart in debug mode
   * minikube delete 
   * minikube start --driver=docker --v=7 --alsologtostderr  
   * minikube status

* kubectl commands
   * kubectl get nodes
   * kubectl get pod
   * kubectl get services
   * kubectl create deployment nginx-depl --image=nginx
   * kubectl get deployment
   * kubectl get replicaset
   * kubectl edit deployment nginx-depl

* debugging
   * kubectl logs {pod-name}
   * kubectl exec -it {pod-name} bash

* create mongo deployment
   * kubectl create deployment mongo-depl --image=mongo
   * kubectl logs mongo-depl-{pod-name}
   * kubectl describe pod mongo-depl-{pod-name}    

* delete deplyoment
   * kubectl delete deployment mongo-depl
   * kubectl delete deployment nginx-depl

* create or edit config file
   * vim nginx-deployment.yaml
   * kubectl apply -f nginx-deployment.yaml
   * kubectl get pod
   * kubectl get deployment

* delete with config
   * kubectl delete -f nginx-deployment.yaml
   * kubectl top: The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, 
     or for a particular pod or node if specified.      
