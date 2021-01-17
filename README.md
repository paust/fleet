
# JKU-CloudComputing-WS20_21 
Repository for the course Cloud Computing at the JKU in the winter semester 2020/2021

# Demo Application

Main Parts of Flux Demo:

https://github.com/paust/fleet.git  
https://github.com/paust/prod.git  
https://github.com/paust/stage.git  
https://github.com/paust/podinfo.git   
https://github.com/vfarcic/devops-toolkit.git  


## Fleet repo  

The fleet repo is responsible for the configuration of flux on the cluster. Here are the repos defined which should be watched, and which Kustomizations should be applied on the Cluster.

## Podinfo  

The podinfo repo is a fork from https://github.com/stefanprodan/podinfo.git and adopted for our need to work two environments.  

## devops-toolkit
The devops-toolkit repo is a demo application from Viktor Farcic where some helm releases are configured.

The prod and the stage repo are configuring the helm versions for the applications on the staging and production evnironments.
These two configuration repos only make sense where helm releases are used to deploy the applications.

## Versioning stragegies for podinfo and devops-toolkit applications

### devops-toolkit  
The devops-toolkit is versioned using helm charts. Which versioin sould be applied to the cluster is configured in the prod/stage repos.The versioning of the app is done in the demo app itself. Pro: the versioning of the running app in the cluster does not inferr the history of the app itself.

### podinfo
 The podinfo applications uses Kustomizations to configure the cluster. The configuration files and the source files/dockerimage are in the same repo. So configuration and the application can only be modified independently. For eg using version 1.2 for the app and version 1.5 for the configuration.... Pro: 



