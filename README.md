# Kubernetes Application Deployment Using Kind on AWS EC2

## Project Overview

This project demonstrates deploying a containerized application to Kubernetes using a Kind (Kubernetes in Docker) cluster hosted on an AWS EC2 instance.

## Technologies Used

- AWS EC2
- Docker
- Docker Hub
- Kubernetes
- Kind
- kubectl
- YAML

## Architecture

Application Source Code → Docker Image → Docker Hub → AWS EC2 → Kind Cluster → Kubernetes Deployment → Service → Application

## Implementation Steps

1. Cloned the application source code from an existing Git repository.
2. Built a Docker image for the application.
3. Pushed the image to Docker Hub.
4. Created an AWS EC2 instance for Kubernetes practice.
5. Installed Docker, Kind, and kubectl.
6. Created a Kind Kubernetes cluster.
7. Created a dedicated Kubernetes namespace.
8. Deployed the application using a Deployment manifest.
9. Configured a Kubernetes Service to expose the application.
10. Verified the cluster, pods, deployment, and service using kubectl.

## Kubernetes Manifests

- `namespace.yml` — Creates a dedicated namespace.
- `deployment.yml` — Defines the application image, replicas, and container configuration.
- `service.yml` — Defines how the application is exposed within or outside the cluster.
- `config.yml` — Kind cluster configuration, if applicable.

## Validation

The deployment was tested using Kubernetes commands such as:

```bash
kubectl get nodes
kubectl get pods -n <namespace>
kubectl get deployments -n <namespace>
kubectl get services -n <namespace>
```

## Evidence

Refer to the `screenshots/` directory for evidence of the cluster, running workloads, services, and application.

## Project Status

Completed as a hands-on learning project. The EC2 instance is stopped when not in use, so the application is not continuously available online.

## Learning Outcomes

- Container image build and distribution.
- Kubernetes cluster creation using Kind.
- Kubernetes namespaces, Deployments, and Services.
- Writing and applying Kubernetes YAML manifests.
- Deploying and validating a containerized application on AWS EC2.

## Credits

The application source was cloned from an existing repository. The original project is credited here: [Original repository URL].

My contribution: container image workflow, Kind cluster setup, Kubernetes manifests, deployment, and validation.
