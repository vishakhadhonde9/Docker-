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
