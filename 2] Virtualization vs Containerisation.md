# Containerization - 
- Containerization is a software deployment process that bundles an application’s code with all the files and libraries it needs to run on any infrastructure.
- Traditionally, to run any application on your computer, you had to install the version that matched your machine’s operating system.
- Containerization is a technology that allows you to package an application and its dependencies (like libraries, frameworks, and configuration files) into a single lightweight, portable unit called a container.
- Containers can run consistently across different environments, such as a developer's laptop, testing servers, or production systems.


# Virtualization vs Containerisation -
##### 1. Resource Efficiency - 
- Virtualization:
     - Each virtual machine (VM) runs its own operating system (OS), which consumes significant resources (CPU, memory, and storage).
     - The hypervisor also adds overhead to manage VMs.

- Containerization:

     - Containers share the host OS kernel, eliminating the need for a full OS in each instance.
     - This reduces resource consumption, allowing more containers to run on the same hardware compared to VMs.


#### 2. Startup Speed -
- Virtualization:
     - Starting a VM requires booting its OS, which can take several minutes.

- Containerization:
    - Containers start almost instantly because they do not boot a full OS but instead share the host's OS kernel.

#### 3. Portability -
- Virtualization:
     - VMs are portable but may face compatibility issues due to differences in hypervisor implementations or underlying infrastructure.
- Containerization:
    - Containers are highly portable. They run consistently across different environments (development, testing, production) as long as a container runtime (e.g., Docker) is present.


| Feature            | Virtualization (VMs)            | Containerization                     |
|--------------------|----------------------------------|---------------------------------------|
| **Overhead**       | High (full OS for each VM)      | Low (shared OS kernel)               |
| **Startup Time**   | Minutes                        | Seconds                              |
| **Portability**    | Limited                        | Highly portable                      |
| **Scalability**    | Slower                         | Fast and efficient                   |
| **Isolation**      | Strong (OS-level)              | Lightweight but effective (process-level) |
| **Resource Usage** | Higher                         | Lower                                |
