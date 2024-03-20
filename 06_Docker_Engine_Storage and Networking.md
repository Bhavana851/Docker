# Docker Engine 

installing Docker on a machine, you are actually installing three different components. 

- Docker Deamon: backgroud process that manages docker objects 

- REST API: interface that programs can use to talk to the docker deamon

- Docker CLI: command line interface used by users.

![Docker Engine](https://static.wixstatic.com/media/1cd646_81d6c571c7d546b7a694fb7f423c3cd4~mv2.png/v1/fill/w_350,h_265,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/1cd646_81d6c571c7d546b7a694fb7f423c3cd4~mv2.png)
- We can have your Docker CLI on another machine, and access the Docker Engine of another machine via the REST APIs. 
- We can use the following command for it.

![Docker Engine](https://static.wixstatic.com/media/1cd646_7a5932460f2d47f6a4ea872dc9a6471f~mv2.png/v1/fill/w_740,h_287,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/1cd646_7a5932460f2d47f6a4ea872dc9a6471f~mv2.png)
``` >> docker -H=remote_docker_engine_ip:port ```



# Networking 

- When we install docker on your machine (host), it creates three networks automatically.
- we can specify the network configs when running the Docker Run command

``` >> docker run ubuntu ```

``` >> docker run ubuntu --network=none ```

``` >> docker run ubuntu --network=host ```

Three Networks 

# 1. Bridge (The default network the container gets attached to)

# 2. None

# 3. Host

![Networking](https://static.wixstatic.com/media/1cd646_19d00bdb9f3c48a38147a9a61fd35678~mv2.jpg/v1/fill/w_740,h_480,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/1cd646_19d00bdb9f3c48a38147a9a61fd35678~mv2.jpg)

# 1. Bridge Network

- This is a private internal network created by docker, on the host.
-  All containers in the host, gets attached to this network by default and gets an internal IP in the range of 172.17.x.x series. 


- If you wish to connect to a container externally, you will have to map the ports from the container to a port available on the host. 


# How to create multiple internal bridge networks?


- By default, docker only creates in Bridge network for all containers.
- You can do this by creating your own network and assigning containers to it.


- Use the following command to create a network.

```  >> docker network create --driver bridge --subnet  180.10.0.0/16 any-customer-name ```

- You can view all available networks by running this command.

```  >> docker network ls ```

- You can view the network details of a container by running the inspect command.

```  >> docker inspect containerID/containerName ```

# 2. Host Network

- If you run the container in the Host network mode,
- this takes out any isolation between the Docker container and the Docker host.
-  If we run the container on Port 5000, this can be accessed using the Host's network and same Port.


# 3. None Network

- The containers are not attached to any network. Each container is isolated on its own.


![n](https://github.com/Bhavana851/Docker-Practice/assets/153347669/dc0d7070-6de3-4767-8638-06d05753680e)


![u](https://github.com/Bhavana851/Docker-Practice/assets/153347669/85d08f0f-2dbe-49e0-9ff1-0fea9b556bf3)

![i](https://github.com/Bhavana851/Docker-Practice/assets/153347669/1963e6e1-aae6-4aa8-8633-808b027c7e34)



# Embedded DNS in Docker

- Container can reach each other using their container names.
- No need to refer to each container by its internal IP.
- If I have a MySQL server running, I can connect to it from another container using the container name of the MySQL server container. 


- The advantage of using the container name is that, 
  in case the host restarts or the container restarts, the internal IP addresses may change.


![e](https://github.com/Bhavana851/Docker-Practice/assets/153347669/51664030-3138-4f0d-94dc-d97cc685b8ca)
















