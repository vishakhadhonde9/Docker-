# Docker Compose -
- Docker Compose is a tool that helps you run multiple Docker containers together as one application.
- Instead of starting each container manually, you can define everything in one file (docker-compose.yml) and start them all with a single command.
- Docker Compose file (docker-compose.yml) is a YAML file where you define the services, networks, and volumes for your multi-container Docker application.
- It tells Docker Compose how to build and run your application with all its components.

# Structure of docker-compose.yml File -

    services:  # Define the services (containers) that make up your app
      service_name:  # Name of the service (e.g., 'web', 'db')
        image: image_name  # The Docker image to use for this service
        build: .  # Optional: Directory with Dockerfile if you need to build an image
        ports:  # Expose ports
          - "host_port:container_port"
        environment:  # Optional: Set environment variables
          - VAR_NAME=value
        volumes:  # Optional: Mount volumes (shared file storage)
          - volume_name:/path/in/container
        networks:  # Optional: Attach service to a custom network
          - network_name
        depends_on:  # Optional: Specify services that must start before this one
          - other_service
        restart: always  # Optional: Define the restart policy
    
    networks:  # Define custom networks (if needed)
      network_name:
        driver: bridge  # Default driver is 'bridge', but you can use others like 'host'
    
    volumes:  # Define named volumes (for persistent data storage)
      volume_name: {}  # Define a volume (could be empty or with settings)
    






# Example-
    
    services:
      web:
        image: nginx
        ports:
          - "80:80"
      db:
        image: mysql
        environment:
          MYSQL_ROOT_PASSWORD:Pass@1234
        port:
           - "3306"
