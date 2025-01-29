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




# Commands of Docker Compose -

## 1. docker-compose up -
- To bilds, creates, starts, and attaches to containers for a service defined in the docker-compose.yml file.

      docker-compose up
      docker-compose up -d

## 2. docker-compose down -
- Stops and removes the containers, networks, and volumes created by docker-compose up.

      docker-compose down
      docker-compose down -v     # to remove volume

## 3. docker-compose start -
- Starts existing containers defined in the docker-compose.yml file.

       docker-compose start

## 4. docker-compose stop -
- Stops running containers without removing them.

       docker-compose stop

## 5. docker-compose logs -
- Displays the logs of the services defined in docker-compose.yml. -

      docker-compose logs

## 6. docker-compose ps -
- Lists the containers that are part of the services defined in the docker-compose.yml file.

      docker-compose ps










