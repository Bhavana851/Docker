# How to create a own Image 

1.OS -Ubuntu

2.update app repo

3.Instal the dependencies using apt

4.Instal the python dependencies using pip

5.Copy the source code to/opt folder 

6.Run web server using "flask"Command

# dockerfile
```
FROM ubuntu

RUN apt-get update

RUN apt-get install python

RUN pip install flask

RUN pip install flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run 
```

```
docker build Dockerfile -t bhavana/my-custom-app 
docker push bhavana/my-custom-app -----------> Docker registry
```

# Dockerfile

![Dockerfile](https://static.wixstatic.com/media/1cd646_d0aba69fbb804aca97747e14ebc0412b~mv2.png)

