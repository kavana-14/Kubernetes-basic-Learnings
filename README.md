# Kubernetes-basic-Learnings
<br>
Creating this repo to tell about my recent basic kuberenetes learnings.
<br>
Kubernetes is a portable, extensible and open-source container orchestration tool that allows you to run and manage container-based workloads and services. <br>
It helps in automating deployment, scaling and management of containerized applications. 
<br>
<b>Problem with containers:</b> 

  Nature of container is scope to single host 

Containers are ephemeral (short-lived) in nature. They can die and revive at any time. If there are less resources or any issues with container (like image is not pulling) container will immediately die. 

Doesn’t support auto healing 

If someone kill the container, can’t access the application. User has to manually look into it. 

Doesn’t support auto scaling 

Load balancing when the load increases 

Doesn’t provide Enterprise support 

Load balancing, firewall, api gateway, auto scaling and healing are not supported by container. 
