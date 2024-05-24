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
![alt text]()



