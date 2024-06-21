# Node.js Hello World Application

## Overview
This repository contains a Node.js "Hello World" application, dockerized and deployed to a Kubernetes cluster using Helm and ArgoCD for GitOps management.

## Prerequisites
- Git
- Docker
- Kubernetes Cluster(I have used minikube)
- Helm
- ArgoCD

## Steps used in project
1. Clone the repository:
   ```sh
   git clone https://github.com/johnpapa/node-hello.git
   cd node-hello
2. Create a multistage docker file
3. Create Github actions workflow and setup environment variables(secreat keys)
4. Push to github repository
5. Install and create a helm chart
6. Modify 'values.yaml' (edit repository name , service type, port and target port)
7. Edit Deployment and Service Templates
8. Create ArgoCD Application YAML file
9. Push to Github repository
10. Deploy with argoCD
11. setup port forwording(kubectl port-forward svc/argocd-server -n argocd 8080:443)
12. get username and password(username will be admin and to get password give (kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo))
13. Apply ArgoCD Application YAML

This project demonstrates how to dockerize a Node.js application, create a Helm chart for Kubernetes deployment, and manage the deployment using ArgoCD.

