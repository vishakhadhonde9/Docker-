

# DOCKER -
- It is an open source centralized platform designed to create, deploy and run applications.
- Docker is written in the Go language.
- Docker uses containers on host O.S to run applications.
- It allows applications to use the same Linux kernel as a system on the host computer, rather than creating a whole virtual 0.S.
- We can install Docker on any 0.S. but the docker engine runs natively on Linux distribution.
- Docker performs O.S level Virtualization also known as Containerization.
- Before Docker many users face problems that a particular code is running in the developer's system but not in the user system.
- It was initially released in March 2013, and developed by Solomon Hykes and Sebastian Pahl.
- Docker is a set of platform-as-a-service that use 0.S. level Virtualization, where as VM ware uses Hardware level Virtualization.
- Container have O.S files but its negligible in size compared to original files of that O.S.

# Container -
- Container is nothing but, it is a virtual machine which does not have any 0S
- A container is like a lightweight, standalone package that contains everything needed to run a piece of software.
- It includes the application code, runtime, system libraries, and dependencies.
- Docker is used to create these containers.


# Docker Image - 
- It is a kind of ready-to-use software read-only template Images is made with source codes, iibraries, external dependencies, and tools.
- Images can not be updated.
- If you want to make change in image you have to create new image.
- Images can not run directly.
- A Docker image is a lightweight, standalone, and executable package that includes everything needed to run a piece of software.

## Structure of a Docker Image -
- Docker image consists of:
     - Base Layer: The foundational layer, often an operating system (e.g., ubuntu or alpine).
     - Additional Layers: Added layers that include dependencies, application code, and configurations.
     - Metadata: Describes the image and its properties, such as environment variables, entry points, and exposed ports
