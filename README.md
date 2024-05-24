# Kubernetes-basic-Learnings
<br>
Creating this repo to tell about my recent basic kuberenetes learnings.<br>
<br>
<b></b>Kubernetes</b> is a portable, extensible and open-source container orchestration tool that allows you to run and manage container-based workloads and services. <br>
It helps in automating deployment, scaling and management of containerized applications. 
<br>
<br>
<b>Problem with containers:</b> 

  <b>1. Nature of container is scope to single host</b>

Containers are ephemeral (short-lived) in nature. They can die and revive at any time. If there are less resources or any issues with container (like image is not pulling) container will immediately die. 

  <b>2. Doesn’t support auto healing</b> 

If someone kill the container, can’t access the application. User has to manually look into it. 

  <b>3. Doesn’t support auto scaling</b> 

Load balancing when the load increases 

  <b>3. Doesn’t provide Enterprise support </b>

Load balancing, firewall, api gateway, auto scaling and healing are not supported by container. 
<br>
<br>

![Screenshot (50)](https://github.com/kavana-14/Kubernetes-basic-Learnings/assets/163102550/941c186a-3a58-4b4f-b606-40cd68b53eec)

<br>
<center><b>Components of Kubernetes Cluster</b></center>
<br>

<b>why Kubernetes? </b>
<br>
In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start 
<br>
Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. 
<br>
<br> 
<b>Cluster: </b>
By default, Kubernetes is a cluster (group of nodes), if any faulty nodes are 	present in a Kubernetes, immediately it will move the pods to another node. 
<br>
<b>Auto Scaling: </b>
Kubernetes has a replica set (replication controller). In this case there is no 	need to deploy a new container. In the deployment YAML file we can increase 	 the replica manually. 
<br>
Kubernetes also support automatic scaling like HPA (Horizontal Pod Auto 	Scale), if the load increases, then it will spin up new container. 
<br>
<b>Auto healing: </b>
Whenever there is damage, Kubernetes must control and fix it. Whenever API 	server receives a signal that any container (pod) is going down, even before it 	goes down, Kubernetes will roll out a new container (pod). 
<br>
<b>Enterprise support: </b>
Enterprise level container orchestration platform (Kubernetes) 
<br>
<b>What is Pod. Why do we deploy applications as a pod in Kubernetes? </b>
It is described as a “Definition of how to run a container”.  <br>
A pod can be a single or multiple containers. In Kubernetes, everything will deal with YAML files. Pod contains yaml file for how to run the container. <br>
If we put 2 containers inside a pod, Kubernetes will ensure that container can have shared network and shared storage. <br>

Example: Container A and B inside a single pod can talk to each other on a localhost. <br>

  ![pod](https://github.com/kavana-14/Kubernetes-basic-Learnings/assets/163102550/e6f1122f-ff7a-4f2f-89c3-b117ebbd81e8)
<br>
Kubernetes allocates cluster IP addresses to pod, we can access the application inside the container using this pod cluster IP address. Kube proxy generates IP addresses. <br>
