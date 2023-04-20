# container-app

Technical Workshop for WiCS (04/19/2023) on "Building your First Microservice".

Presentation Link: https://docs.google.com/presentation/d/1qLVPS8uzBnwc8dTpHIP7hpOxZNr4WH1ZxC9Au6vjsQo/edit?usp=sharing

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Running the Application](#running-the-application)

## Introduction

This is a simple web application made using Flask in Python. It is a simple "Hello, World!" application that displays a message on the home page. It is packaged as a Docker container and can be deployed to a Kubernetes cluster. 

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Kubernetes](https://kubernetes.io/docs/tasks/tools/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [Python](https://www.python.org/downloads/)

## Getting Started

1. Clone the repository

```bash 
git clone https://github.com/kuhuhalder/container-app.git
```

2. Change directory into the repository

```bash
cd container-app
```

3. Create a virtual environment

```bash
python3 -m venv venv
```

4. Activate the virtual environment

```bash
source venv/bin/activate
```

5. Install the dependencies

```bash
pip3 install -r requirements.txt
```

## Running the Application

1. Run the application

```bash
python3 app.py
```

2. Open the application in your browser at http://localhost:5000

3. Stop the application by pressing `Ctrl + C`

4. Build the Docker image

```bash
docker build -t container-app .
```

5. Run the Docker container

```bash
docker run -d -p 8000:5000 container-app
```

6. Open the application in your browser at http://localhost:8000

7. Stop the Docker container

```bash
docker stop <container-id>
```

8. Delete the Docker container

```bash
docker rm <container-id>
```

9. Delete the Docker image

```bash
docker rmi container-app
```

10. Start Minikube

```bash
minikube start
```

11. Create a Kubernetes deployment

```bash
kubectl create deployment container-app --image=container-app
```

12. Expose the deployment as a service

```bash
kubectl expose deployment container-app --type=NodePort --port=5000
```

13. Get the URL of the service

```bash
minikube service container-app --url
```

14. Open the application in your browser at the URL

15. Delete the Kubernetes deployment

```bash
kubectl delete deployment container-app
```

16. Delete the Kubernetes service

```bash
kubectl delete service container-app
```

17. Stop Minikube

```bash
minikube stop
```





