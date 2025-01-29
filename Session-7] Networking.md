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

## 5. Connect with Additional Network -
 - docker network connect command is used to attach a running container to an additional Docker network.
 - This is useful when you want to connect a container to more than one network.

         docker network connect NETWORK CONTAINER

         docker network disconnect NETWORK CONTAINER



## Run Container Within Specific Network-


        docker run -d --name container1 --network network_name image_name




# Proxy Server-
- proxy server is an intermediary server that sits between a client and a destination server. It processes requests and responses.
- proxy server can act as a load balancer, particularly in the case of a reverse proxy.

## Uses of Proxy Servers:
- Privacy and Anonymity: Hiding your IP address and browsing activity.
- Access Control: Filtering or restricting access to certain websites.
- Caching: Reducing bandwidth by storing copies of frequently accessed resources.
- Security: Protecting internal systems by acting as a barrier against attacks.

## Types of Proxy Servers:
- **Forward Proxy:** Used by clients to access external resources. It hides the client's IP address from the target server.
- **Reverse Proxy:** Used by servers to manage incoming client requests. It can distribute traffic, provide load balancing, or improve security.
- **Transparent Proxy:** Does not hide the user's IP address; often used for caching or filtering.

# Nginx Proxy Server -
- Add following configuration in nginx.conf:


                http {
                    # Include mime types
                    include /etc/nginx/mime.types;
                    default_type application/octet-stream;
                
                    # Define the upstream group of servers
                    upstream webserver {
                        server c1:80; # Backend server 1
                        server c2:80; # Backend server 2
                    }


- Add following configuration in default.conf:


                location / {
                    proxy_pass http://webserver;
                    proxy_set_header Host $host;
                    proxy_set_header X-Real-IP $remote_addr;
                    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
                }
                
