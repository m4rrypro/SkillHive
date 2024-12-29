# Docker Basics

Docker is a platform that simplifies the process of building, packaging, and deploying applications in lightweight, portable containers. In this section, we’ll cover the basics of Docker, its components, and key commands you’ll need to get started.

---

## What is a Container?

A container is a lightweight, standalone, and executable software package that includes all the dependencies (libraries, binaries, and configuration files) required to run an application. Containers isolate applications from their environment, ensuring they work consistently across different systems.

---

## Docker Components

There are three key components in the Docker ecosystem:

1. **Dockerfile**  
   A text file containing instructions (commands) to build a Docker image. It acts as a blueprint for creating Docker images.

2. **Docker Image**  
   A snapshot of a container, created from a Dockerfile. Images are stored in a registry, such as Docker Hub, and can be pulled or pushed to the registry.

3. **Docker Container**  
   A running instance of a Docker image. Containers are portable, lightweight, and provide isolation for applications.

---

## Docker Commands

Below are some essential Docker commands you’ll use frequently:

1. **Pull an image**
   ```bash
   docker pull <image>
   ```
   Downloads an image from a registry, like Docker Hub.

2. **Build an image**
   ```bash
   docker build -t <image_name> <path>
   ```
   Builds an image from a Dockerfile, where `<path>` is the directory containing the Dockerfile.

3. **List images**
   ```bash
   docker image ls
   ```
   Lists all images available on your local machine.

4. **Run a container**
   ```bash
   docker run -d -p <host_port>:<container_port> --name <container_name> <image>
   ```
   Runs a container from an image, mapping host ports to container ports.

5. **List running containers**
   ```bash
   docker container ls
   ```
   Lists all currently running containers.

6. **Stop a container**
   ```bash
   docker container stop <container>
   ```
   Stops a running container.

7. **Remove a container**
   ```bash
   docker container rm <container>
   ```
   Removes a stopped container.

8. **Remove an image**
   ```bash
   docker image rm <image>
   ```
   Removes an image from your local machine.

---

This section provides the foundational knowledge and tools to start working with Docker. Practice these commands and explore Docker’s components to get comfortable with containerized application development.