## 1.Difference Between Virtualization and Containerization 

**Virtualization:**

* Running multiple virtual machines(VMs) on the single physical server,each with its own Operating system.it's like having separate houses with different families in a single building.

**Containerization:**

* Running isolated applications (containers)on a shared operating system,its like having apartments in a single building,where each apartment is self contained but shares the common infrastructure.


![V AND C](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcR5GtFwToXMn3YJG7v5DysJm3y1atXArdPt3Tu4_YKHhizGCDTE)


## 2.What problem does the Docker solve


Docker solve the problem of consistent,portable,and the efficient application deployment by packing the applications and their dependencies into containers ensuring they run reliably across the **different environments and the systems while maintaining security and scalability.**

![Docker](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSxuc-a3hiWgUtc4rzxVvrX5XJlf_cOVTCIYUvvhrvqg9ZSKPtR)


## 3.What is Dockerfile and  Why do you use it 

A Dockerfile is a Script that defines the steps to create a Docker container image.

it is used to automate the containerization of an application,making it reproduciable and shareable.

![Dockerfile](https://docs.docker.com/build/guide/images/layers.png)


## 4.Explain the workflow of how a Docker container is created?

Docker Container Creation workflow 

1.Dockerfile:Create the Dockerfile with application instructions  

2.Build Image:use Docker build to build an image from 
Dockerfile 

3.Run Container:Run container from the image using docker run.

4.Container:container runs your application,isolated and self contained.

**How to manage the multiple containers** 

By using the container orchestration tools like Kubernetes  to manage multiple containers ensuring high availability,scalability and LoadBalancing.

![wfdocker](https://miro.medium.com/v2/resize:fit:640/format:webp/1*jN1jj-fdEZAwE28BobvRSA.jpeg)
