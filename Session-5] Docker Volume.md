# Docker Volume -
-  Docker volume is a persistent storage mechanism used by Docker containers to store and share data between containers or with the host system.
-  Volumes allow data to persist even when containers are stopped, removed, or recreated, and they are managed by Docker itself.
-  Docker volumes are stored outside of the container's filesystem(VM), which ensures data persists even if the container is removed.
-  Volumes can also be shared between multiple containers.

# Docker Volume Types-
  ## Bind Mount -
  -  Bind mount in Docker is a way to mount a specific file or directory from the host machine into a container.
  -  The directory or file is directly mapped from the host filesystem into the container.
  -  Any changes made to the file or directory on the host are immediately reflected in the container.
  -  Bind mounts require you to provide an absolute path from the host system.

              docker run -v /path/on/host:/path/in/container <image_name>

- You can create own directory and add here /path/on/host 
  ## Named Volume -
  - Named volumes allow you to persist data outside the lifecycle of containers and are typically used when you want Docker to handle the volume's storage location and management.
  - These volumes are useful for storing and sharing data between containers, and they can be named explicitly, which provides a convenient way to refer to them.
- 1. Create Named Volume-

          docker volume create <volume_name>

     - Check Volume is created :

            docker volume ls

- 2. Use a Named Volume with a Container
     - To use a named volume when starting a container, you use the -v or --mount flag.
    
              docker run -v <volume_name>:<path_in_container> <image_name>
