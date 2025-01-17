# Dockerfile -
- Dockerfile is a script-like text file containing a series of instructions on how to build a Docker image.
- Dockerfiles are used to create container images, which can be used to package software and run it in different environments.
- These instructions specify how the image should be created, including the base operating system, application dependencies, configuration, and the command to run the application.

## What's in a Dockerfile? -
# Use the official Ubuntu base image
FROM ubuntu:22.04

# Set the working directory inside the container
WORKDIR /app

# Copy a shell script into the container
COPY hello.sh .

# Grant execution permissions for the shell script
RUN chmod +x hello.sh

# Command to execute the shell script
CMD ["./hello.sh"]

#### 1. Base Image (FROM) -
- Specifies the starting point for the image. This could be a lightweight operating system or a preconfigured environment

#### 2. Maintainer/Labels (LABEL) -
- (Optional) Adds metadata about the image, such as author information.

#### 3. Working Directory (WORKDIR) -
- Sets the directory inside the container where commands will execute.

#### 4. Copy Files (COPY or ADD) -
Copies files from the host machine to the container.

#### 5. Install Dependencies (RUN)
Runs commands during the image build process, such as installing software or dependencies.

#### 6. Environment Variables (ENV)
Sets environment variables inside the container

#### 7. Expose Ports (EXPOSE)
Declares the network ports the container listens on.

#### 8. Command to Run (CMD)
Specifies the command to execute when the container starts.

#### 9. Volumes (VOLUME)
(Optional) Creates a mount point for persistent storage.
