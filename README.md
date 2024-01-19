# PoC

# Kubernetes Hello World Setup Guide

Step-by-step instructions to set up a Kubernetes application with a Hello World web server.

## Prerequisites
- Install Docker
- Install Minikube

## Steps
#Start Minikube:

  minikube start

#Create an index.html file: 
  
#Build the Docker image:

 docker build -t hello-world-webserver .

#Create the Pod:

 kubectl apply -f hello-world-pod.yaml  
 
#Create the Service:

 kubectl apply -f hello-world-service.yaml
 
#Port Forwarding:

 kubectl port-forward service/hello-world-service 8080:80
  
  Access the application at http://localhost:8080

#Load Balancer (Minikube):

minikube service hello-world-service

This will open the service in your default web browser.
 
