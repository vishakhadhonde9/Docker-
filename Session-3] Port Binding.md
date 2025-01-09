# Port Binding -
- Port binding in Docker allows you to expose a container's internal ports to the host system, enabling access to the services running inside the container.
- This is typically achieved using the -p or --publish option during container creation.

## How Port Binding Works -
- A Docker container runs in its own isolated network namespace.
- When you bind a container port to a host port, the host system forwards traffic from the host port to the container's port.

      docker run -p <host_port>:<container_port> Image_Name/id
  

- Every container have its own unique ports.
- For example, container1 have its own port 80 and container2 also having its own port 80.


       docker run -d -p 80:80 nginx

  - Access the Service -

       curl http://localhost:80
  
### Expose Multiple port -
       
        docker run -d -p 80:80 -p 8443:443 nginx


## Docker inspect command -
- docker inspect command retrieves detailed information about a Docker container in JSON format.
- This information includes configuration details, networking, storage, environment variables, and more.

       docker inspect CONTAINER_ID

## ufw command -
- with UFW (Uncomplicated Firewall), a simple tool for managing firewall rules.
         sudo ufw allow 80
- this allow port 80


