# Three-Tier Application with Docker and Kubernetes

## Overview

This project implements a three-tier application architecture using Docker and Kubernetes. The application consists of three key components: a backend, a database, and a proxy server. The backend is built using a multi-stage Dockerfile for optimized performance, while the database and proxy services are securely configured with host machine credentials. Additionally, the entire project is orchestrated in Kubernetes with each tier deployed as a scalable, highly available service.

## Features

- **Multi-stage Dockerfile**: Efficient and secure image for the backend application.
- **Kubernetes Deployments**: Each tier (Proxy, Backend, Database) is deployed with 2 replicas for high availability.
- **Namespace Management**: The project runs in a dedicated Kubernetes namespace: `webapp`.
- **Secure Database Credentials**: Credentials are securely mounted from the host machine using Kubernetes secrets.
- **Proxy over HTTPS**: Proxy service is configured to run over HTTPS with host-based configuration files.
- **Single Command Orchestration**: Bring up and down the entire application stack with one command using Docker Compose.

## Architecture

The three-tier architecture consists of the following:

- **Backend**: Serves the core application logic, deployed in a Kubernetes deployment with 2 replicas.
- **Database**: Stores application data, configured to securely use credentials from the host machine and deployed with 2 replicas.
- **Proxy**: Acts as a gateway, serving traffic over HTTPS and forwarding requests to the backend service.


