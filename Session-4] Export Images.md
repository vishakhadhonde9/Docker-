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
