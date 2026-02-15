# Day-01: Docker & Kubernetes Basics

## Target: CKA (Certified Kubernetes Administrator)

---

## Docker

### What is Docker?

Docker is a platform used to build, ship, and run applications inside containers.

It helps developers package applications along with all required dependencies into a standardized unit called a container.

---

## What is a Container?

A container is a lightweight, isolated environment that:

- Shares the host OS kernel
- Contains application code, libraries, and dependencies
- Starts quickly
- Uses fewer resources than a virtual machine

---

## Docker Workflow

Dockerfile 26 Docker Image 26 Push to Registry 26 Pull 26 Run in Dev/Test/Prod

Flow Explanation:

1. Write a Dockerfile
2. Build Docker Image
3. Push image to Docker Registry (DockerHub / Private Registry)
4. Pull image in different environments
5. Run container

---

## Why Use Containers Instead of Virtual Machines?

| Containers | Virtual Machines |
|------------|------------------|
| Share OS Kernel | Each VM has full OS |
| Lightweight | Heavy |
| Faster startup | Slow startup |
| Better resource utilization | Resource under-utilization |

Containers provide isolation while efficiently sharing infrastructure resources.

---

# Kubernetes

Kubernetes is a container orchestration tool.

It manages containerized applications across a cluster of machines.

---

## Key Features of Kubernetes

### Container Orchestration
Manages:
- Container lifecycle
- Scheduling
- Scaling across multiple nodes

### Self-Healing
- Restarts failed containers
- Replaces unhealthy pods
- Reschedules containers automatically

### Automated Scaling
- Scales applications up/down based on demand

### Service Discovery & Load Balancing
- Exposes containers via DNS name or IP
- Distributes traffic automatically

### kubectl
`kubectl` is the CLI tool used to:
- Deploy applications
- Manage cluster resources
- Interact with Kubernetes API server

