# How to create Docker Image from Container-
- docker commit command is used to create a new Docker image from an existing container.
- It captures the current state of the container, including all the changes made to it, and saves it as an image that you can reuse later.

          docker commit <container-id/name> NEW_IMAGE_NAME

- -a, --author: Add author metadata to the image.

          docker commit -a "Your Name" my-container my-new-image 

- -m, --message: Add a commit message to describe the changes.

         docker commit -m "Installed Apache and updated configuration" my-container my-new-image
  

## Method-1] Store Image into tar file -
- docker save command is used to save a Docker image to a tar archive.
- This is useful for transferring images between systems or storing them for backup purposes.

 
         docker save -o <output-file>.tar <image-id>
                             OR
         docker save img-id > newfile.tar
- This will create a .tar file containing your Docker image.

### docker export -
- This command is used to export a container's filesystem as a tar archive.
- This command is different from docker save, which saves a Docker image. docker export captures the container's file system (the state of the container’s filesystem at the time of the export), but it does not include the Docker image history, metadata, or volumes associated with the container.


      docker export <container_id_or_name> -o <output_file>.tar
                                   OR
      docker export <container_id_or_name> > newfile.tar

### Copy image on your local machine -

    scp -i <your_key.pem> ubuntu@<ec2_public_ip>:<path_to_image_tar> <local_destination_path>
    

## Method-2] Push image on Docker Hub -
- 1) Login to Docker Hub- 
      - Use the docker login command to authenticate.
     
              docker login

      - Enter your Docker Hub username and password(token) when prompted.
    
- 2) Tag the docker image -
        - Tagging a Docker image is the process of assigning a unique identifier like name to the image so you can manage and version.
        
               docker tag <source-image> <username>/<repository>:<tag>
               e.g.- docker tag cont3img:newimg fortunecloud815/repo1:newimg
          

             
- 3) Push image on Docker Hub -
        - docker push command is used to upload Docker images from your local machine to a container registry, such as Docker Hub, AWS ECR.


               docker push <repository>:<tag>
             

## Method-3] Push image on ECR -
- 1) You have to install awa cli on your system.


                  sudo apt update
                  sudo apt install awscli -y

- 2) Create repository on ECR.
- 3) Authenticate Docker with ECR-

           aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <account-id>.dkr.ecr.<region>.amazonaws.com

- 4) Tag the Docker Image -

           docker tag <image-id> <repository-uri>:<tag>
        

- 5) Push the Image to ECR -

         docker push <repository-uri>:<tag>
     
