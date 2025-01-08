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

## List running containers -
        docker ps

## List all containers (including stopped ones)- 

        docker ps -a
