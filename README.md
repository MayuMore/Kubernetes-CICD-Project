# Kubernetes-CICD-Project
## CI/CD Pipeline using GitHub, EC2, Jenkins, Ansible, Docker, Docker Hub, and Kubernetes
<picture>
  
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://github.com/MayuMore/Kubernetes-CICD-Project/blob/main/src/kubernetes-proj.png">
</picture>


This project demonstrates the implementation of a Continuous Integration and Continuous Deployment (CI/CD) pipeline for deploying a Dockerized application to Kubernetes. The pipeline is built using various technologies including GitHub, EC2, Jenkins, Ansible, Docker, Docker Hub, and Kubernetes.

## Architecture Overview

### GitHub: The source code repository where the application code is stored and version-controlled.

### Jenkins: The CI/CD server responsible for managing the pipeline. It listens for changes in the GitHub repository and triggers the build and deployment process using Github Webhook.

### EC2: The virtual machine hosting the Jenkins server. It is responsible for running Jenkins and executing pipeline stages.

### Ansible: The configuration management tool used to provision and configure the Kubernetes cluster using docker images.

#### Docker: The containerization platform used to package the application and its dependencies into a Docker image.

### Docker Hub: The container registry where Docker images are stored.

### Kubernetes: The container orchestration platform responsible for deploying and managing the application containers.

## Prerequisites
Before setting up the CI/CD pipeline, ensure you have the following prerequisites:

1) A GitHub and dockerhub account
2) EC2 instance no 1 :- Jenkins Installtion
EC2 instance no 1:- Ansible, docker, kubernetes Installtion
EC2 instance no 3:- Docker, Kubernetes installtion
3) SSH Connection configuration between all three servers


## Setup Instructions
Follow these steps to set up the CI/CD pipeline:

1) Clone the repository: https://github.com/MayuMore/Kubernetes-CICD-Project.git
2) Set three EC2 servers using terraform temaplates given in the Installtion_scripts Folder
3) Configure the Jenkins job to listen for changes in the GitHub repository and trigger the build and deployment process. Set up the following stages:- a) git checkout b) sending files to ansible server c) Docker Imagebuilding d) Docker Image tagging e) push images to dockerhub f) copy files from ansible to kubernetes server g) kubernetes deployment using ansible
5) Trigger the jobs to see the deployment.





