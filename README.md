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

  <b>4. Doesn’t provide Enterprise support </b>

Load balancing, firewall, api gateway, auto scaling and healing are not supported by container. 
<br>
<br>

![Screenshot (50)](https://github.com/kavana-14/Kubernetes-basic-Learnings/assets/163102550/941c186a-3a58-4b4f-b606-40cd68b53eec)
<b><center>Components of Kubernetes Cluster</center></b>
<br>

<b>why Kubernetes? </b>
<br>
In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start 
<br>
Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. 
<br>
<br> 
<b>1. Cluster: </b><br>
By default, Kubernetes is a cluster (group of nodes), if any faulty nodes are 	present in a Kubernetes, immediately it will move the pods to another node. 
<br>
<b>2. Auto Scaling: </b><br>
Kubernetes has a replica set (replication controller). In this case there is no 	need to deploy a new container. In the deployment YAML file we can increase 	 the replica manually. 
<br>
Kubernetes also support automatic scaling like HPA (Horizontal Pod Auto 	Scale), if the load increases, then it will spin up new container. 
<br>
<b>3. Auto healing: </b><br>
Whenever there is damage, Kubernetes must control and fix it. Whenever API 	server receives a signal that any container (pod) is going down, even before it 	goes down, Kubernetes will roll out a new container (pod). 
<br>
<b>4. Enterprise support: </b><br>
Enterprise level container orchestration platform (Kubernetes) 
<br>
<br>
<b>What is Pod. Why do we deploy applications as a pod in Kubernetes? </b><br>
It is described as a “Definition of how to run a container”.  <br>
A pod can be a single or multiple containers. In Kubernetes, everything will deal with YAML files. Pod contains yaml file for how to run the container. <br>
If we put 2 containers inside a pod, Kubernetes will ensure that container can have shared network and shared storage. <br>

Example: Container A and B inside a single pod can talk to each other on a localhost. <br>

  ![pod](https://github.com/kavana-14/Kubernetes-basic-Learnings/assets/163102550/e6f1122f-ff7a-4f2f-89c3-b117ebbd81e8)
<br>
Kubernetes allocates cluster IP addresses to pod, we can access the application inside the container using this pod cluster IP address. Kube proxy generates IP addresses. <br>
<br>
<br>
<b>Kubectl: </b><br>

Kubectl is a command line tool for Kubernetes. We can interact with clusters through kubectl. 

<b>Install kubectl for linux- (Ubuntu 22.04)</b><br>

```> curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"```<br><br> 
```> sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl ```<br><br>
```> kubectl version```

<br>
<b>Deploying a Kubernetes Cluster on Virtual Machines:(ubuntu 22.04) </b>
<br>
<b>Prerequisites: </b><br>
<ul>
<li>2 CPUs </li>
<li>Min. 8GB RAM </li>
<li>Create two virtual machines.(control plane and worker node)</li>
</ul>
<br>
<b><p>Installation and setting up of kubernetes nodes:</p></b>
<p>Reference:</p>
<a href="https://rudimartinsen.com/2023/12/29/kubernetes-cluster-on-vms-2024/">Deploying a Kubernetes Cluster</a>
