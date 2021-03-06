Introduction to OpenShift workshop
=====================

![Show Workshop](workshop/content/images/show-workshop.png)

This tutorial will act as step-by-step guide in helping you to understand Openshift concepts. We will deploy applications on top of OpenShift following different methods and in between We will explore some of the key concepts while playing with those Apps. These are the modules that you will find in this guide:


<ol>
<li>Explore the Web Console</li>
<li>Explore the oc CLI</li>
<li>Deploying - Using a container image</li>
<li>Playing with - Application Scaling</li>
<li>Deploying - Using Source-to-image </li>
<li>Playing with - Transfering files</li>
<li>Deploying - Using binary files</li>
<li>Playing with - SSL routes</li>
<li>Deploying - Using Dockerfiles</li>
<li>Playing with - Storage</li>
<li>Deploying - Using Templates</li>
<li>Playing with - Port Forwarding </li>
<li>Deploying - Using hooks</li>
<li>Playing with - Rollback</li>
<li>Deploying - Using CI/CD pipelines</li>
<li>Playing with - Advanced Deployment Stragies</li>
<li>Bonus - Using ODO</li>
<li>Review - Configuring a complete CI/CD Pipeline</li>
</ol>



Deploying the workshop
=====================

*NOTE*: You have to be log in to the OpenShift cluster from where you launch the installer, probably as clusteradmin if you want to run the workshop as multiuser

You need to run this workshop in a working OpenShift Cluster. In order to install it, run the following commands:


`git clone --single-branch --branch master --recurse-submodules https://github.com/luisarizmendi/lab-ocp-intro.git`

`cd lab-ocp-intro`


Now, if you want to run the workshop for any user on the cluster (you need clusteradmin privileges and dynamic storage to launch this one):

`./workshop/launch-workshop.sh`

... or if you just want the environment for you (you have to have a project where to install it already created):

`./workshop/launch-workshop.sh --singleuser`





SINGLE and MULTIUSER modes
=====================

This workshop can work in two modes: single user or multiuser. If you run it as multiuser (default) you will need a dynamic persistent volume storage to make it work. Also take into account that you will need to be log in as CLUSTER ADMIN in OpenShift since multiple projects and users will be created

Singleuser workshop is more restricted since it uses a serviceaccount instead of the "real" ocp user. That could be a problem while using the embedded Web Console (for example if you try to create a project using the Web Console). You can solve this just using the regular Web Console (not the embedded one). In the case of the CLI embedded terminal there is no problem if you just login ('oc login') with your user.


