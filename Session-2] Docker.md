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

## Run MySql Container-

        docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD="Your_Password" --name <cont_name> <img_name/id>

  
## Run Container Interactively -
- -it option in the docker run command is used to run a container interactively, allowing you to interact with it through a terminal

       docker run -it <img_name>

- -i (--interactive): Keeps the container’s standard input (stdin) open, even if not attached
- -t (--tty): Allocates a pseudo-TTY

## List running containers -
        docker ps

## List all containers (including stopped ones)- 

       docker ps -a
       
## Work within Container-
- docker exec command is used to execute a command inside a running container.
- It allows you to interact with a container's processes or environment.

        docker exec [OPTIONS] <Container_name> COMMAND

        e.g.- docker exec my-container ls

- -i, --interactive: Keep the standard input (stdin) open.
- -t, --tty: Allocate a pseudo-TTY, enabling an interactive terminal.

          docker exec -it <container_name> shell_type
          e.g.- docker exec -it my-container /bin/bash
    
- --detach or -d: Run the command in the background.
           

## Start a stopped container- 

       docker start <container_id>

## Stop a running container-

      docker stop <container_id>

## Stop all container-

     docker stop $(docker ps -aq)
    
## Stop Multiple container-
 
      docker stop container1 container2 container3
      
## Remove a container-

     docker rm <container_id>

## Remove all Container-

       docker rm $(docker ps -aq)


## Remove Multiple Container-

      docker rm container1 container2 container3

## Remove an Image-

    docker rmi <image_id>

## Remove Mutiple Images -

    docker rmi image1 image2 image3

## Remove all Images-

       docker rmi $(docker images -q)

   
