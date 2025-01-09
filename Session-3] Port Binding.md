# Port Binding -
- Port binding in Docker allows you to expose a container's internal ports to the host system, enabling access to the services running inside the container.
- This is typically achieved using the -p or --publish option during container creation.

## How Port Binding Works -
- A Docker container runs in its own isolated network namespace.
- When you bind a container port to a host port, the host system forwards traffic from the host port to the container's port.

         docker run -p <host_port>:<container_port> Image_Name/id
  
       
