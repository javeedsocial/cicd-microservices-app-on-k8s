# cicd-microservices-app-on-k8s

cicd-microservices-app-on-k8s

# Kubernetes Deployment with Jenkins

This repository contains a Jenkinsfile for building and deploying a frontend and backend application on Kubernetes. The Jenkins pipeline uses Docker for building the application images and kubectl for deploying them on a Kubernetes cluster.

## Prerequisites

- Jenkins server with Docker installed.
- Kubernetes cluster with `kubectl` configured.
- Jenkins Kubernetes plugin installed (for running the Jenkins agent in a Kubernetes pod).

## Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

Update Jenkinsfile:

Modify the Jenkinsfile according to your application structure and Docker image names.

Configure Jenkins:

Ensure that Jenkins is configured to use a Kubernetes agent.
Install necessary Jenkins plugins, including the Kubernetes plugin.
Create Kubernetes Credentials:

Create a Kubernetes credentials entry in Jenkins for authenticating with your Kubernetes cluster.

Create Jenkins Pipeline:

Create a new Jenkins pipeline job and link it to your repository. Set up the pipeline to use the Jenkinsfile in your repository.

Run the Pipeline:

Trigger the Jenkins pipeline to build and deploy your application. The pipeline will build Docker images and deploy them to your Kubernetes cluster.

Jenkinsfile Overview
The Jenkinsfile defines a Jenkins pipeline with three stages: Build Frontend Image, Build Backend Image, and Deploy.
The Docker images are built using the Dockerfile in the frontend and backend directories.
The kubectl run command is used to deploy the application on Kubernetes.
Additional Notes
Ensure that your Kubernetes cluster is properly configured and has the necessary resources for deploying the application.
Review and update Kubernetes namespace, server URL, and credentials in the Jenkinsfile.
License
This project is licensed under the MIT License.

```
Feel free to further customize the instructions based on your specific project and requirements.
```
