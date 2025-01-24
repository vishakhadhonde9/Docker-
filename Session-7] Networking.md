# Networking in Docker -
- Networking allows containers to communicate with each other and with the outside world.
- Network also provides isolation to your containers.

## Types Of Network -
### 1. Bridge Network (Default)-
- This is the default network mode when you don’t specify any network.
- Containers can communicate to each other on the same Docker host, but not with containers on other networks unless specifically configured.
- It uses virtual Ethernet bridges to connect containers.

### 2. Host Network -
- The container uses the host machine’s network directly (i.e., it shares the host’s IP address).

### 3. Overlay Network -
- This network type is used when containers are spread across multiple machines.
- It allows containers on different hosts to communicate with each other securely.
- Docker manages routing between containers on different hosts using the overlay network.


# Common Docker Network Commands -
## 1. List Networks -

        docker network ls

## 2. Create a Network -
To create a new network with a specific driver (e.g., bridge, overlay, etc.):

      docker network create <network-name>

## 3. Inspect a Network -
To view detailed information about a network (including its settings, containers connected, etc.):

     docker network inspect <network-name>
     
## 4. Create a Network with Custom Settings -


      docker network create \
        --driver bridge \
        --subnet 192.168.1.0/24 \
        --gateway 192.168.1.1 \
        my-custom-network

## Run Container Within Specific Network-


        docker run -d --name container1 --network network_name image_name

