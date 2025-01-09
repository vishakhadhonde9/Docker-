# Commands for creating and managing container-

## Pull the Required Image-
- You need a Docker image to create a container. Pull an image from Docker Hub (if not already downloaded):

          docker pull <image_name>
  
## To Check Docker Imgaes on System-

        docker images 
             OR
        docker image ls
        
## Check Image history -    

        docker history <image_name> or <image_id>
        

## Create and Run the Container -
- docker run command is used to create and start a new container from a Docker image.

          docker run <image_name>

## Run Container in background -
- docker run -d command is used to run a Docker container in detached mode, meaning the container runs in the background rather than in the foreground.

         docker run -d <image_name>

## Run Container with custom name -
- --name option in the docker run command allows you to assign a custom name to the container.
       docker run --name <container_name> -d <img_name>
     

## List running containers -
        docker ps

## List all containers (including stopped ones)- 

        docker ps -a
        
## Start a stopped container- 

       docker start <container_id>

## Stop a running container-

      docker stop <container_id>

## Remove a container-

     docker rm <container_id>

## Remove an image-

    docker rmi <image_id>
