# Underlying Technologies

Understanding the core technologies that power Docker will provide you with a deeper insight into how Docker works and will help you use the platform more effectively.

## Linux Containers (LXC)

Linux Containers (LXC) enables running multiple independent Linux systems on a single computer. Acting as isolated spaces, LXC containers share host resources like memory and processing power, without needing their own full operating system copy, ensuring lightweight and fast startup.

---

### 1. What are Namespaces?

Docker namespaces are a fundamental feature of Linux that Docker uses to create isolated environments for containers. They provide a layer of isolation by creating separate instances of global system resources, making each container believe it has its own unique set of resources. Docker utilizes several types of namespaces, including:

- **PID (Process ID)**: Isolates process IDs, so processes inside a container only see their own.
- **NET (Network)**: Provides separate networking stacks for containers.
- **MNT (Mount)**: Controls access to filesystem mount points.
- **UTS (Unix Timesharing System)**: Allows containers to have their own hostname and domain name.
- **IPC (InterProcess Communication)**: Isolates shared memory segments and semaphores.
- **USER**: Enables mapping container users to host users.

By leveraging these namespaces, Docker can create lightweight, portable, and secure containers that run consistently across different environments.

**Visit the following resources to learn more:**
- [Linux Namespaces Explained](https://man7.org/linux/man-pages/man7/namespaces.7.html)
- [Docker Namespaces Overview](https://docs.docker.com/engine/security/userns-remap/)

---

### 2. What are cgroups?

**Control Groups (cgroups)** is a Linux kernel feature that allows the allocation and management of resources, such as CPU, memory, network bandwidth, and I/O, among groups of processes running on a system. Docker utilizes cgroups to enforce resource constraints on containers, ensuring consistent and predictable behavior.

#### Key Features of cgroups:
- **Resource Limiting**: Restricts CPU, memory, and disk I/O for containers.
- **Resource Isolation**: Prevents one container from affecting the performance of others.
- **Process Tracking**: Keeps track of all processes within a group for better management.

**Visit the following resources to learn more:**
- [Control Groups Overview](https://man7.org/linux/man-pages/man7/cgroups.7.html)
- [Docker cgroups](https://docs.docker.com/config/containers/resource_constraints/)

---

### 3. What is Union File System (UnionFS)?

Union file systems, also known as UnionFS, play a crucial role in Docker's functioning. It creates a virtual, layered file structure by overlaying multiple directories without modifying the original file system. This approach minimizes duplication and reduces container image sizes, optimizing storage performance.

#### Benefits of UnionFS in Docker:
- **Layered Images**: Each Docker image layer is stacked to form a unified view.
- **Storage Optimization**: Reduces redundancy by reusing unchanged layers.
- **Fast Build and Deploy**: Speeds up building and deployment by caching layers.

**Visit the following resources to learn more:**
- [Union File Systems Basics](https://wiki.archlinux.org/title/Union_filesystems)
- [Docker Storage and UnionFS](https://docs.docker.com/storage/storagedriver/overlayfs-driver/)

---