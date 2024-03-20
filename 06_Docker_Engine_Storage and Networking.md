# Docker Engine 

installing Docker on a machine, you are actually installing three different components. 

- Docker Deamon: backgroud process that manages docker objects 

- REST API: interface that programs can use to talk to the docker deamon

- Docker CLI: command line interface used by users.

![Docker Engine](https://static.wixstatic.com/media/1cd646_81d6c571c7d546b7a694fb7f423c3cd4~mv2.png/v1/fill/w_350,h_265,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/1cd646_81d6c571c7d546b7a694fb7f423c3cd4~mv2.png)
- We can have your Docker CLI on another machine, and access the Docker Engine of another machine via the REST APIs. 
- We can use the following command for it.

![Docker Engine](https://static.wixstatic.com/media/1cd646_7a5932460f2d47f6a4ea872dc9a6471f~mv2.png/v1/fill/w_740,h_287,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/1cd646_7a5932460f2d47f6a4ea872dc9a6471f~mv2.png)
# >> docker -H=remote_docker_engine_ip:port

