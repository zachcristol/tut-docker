# Running docker image

We will be using a basic node image to run a simple JS server (/src/index.js)  

### Dockerfile

```
# What docker image to build on. Find this on hub.docker.com: https://goo.gl/m8GKco
FROM  node:10.14.2
# Specifies that the running docker image will expose the port :8080.
# This is because our js app listens on port :8080
EXPOSE 8080
# Copy index.js into the root directory of the container
COPY src/index.js .
# Commands to be run when the container starts
CMD node index.js
```


### Command Line

#### Building an image
From the directory that ```Dockerfile``` is in run...  
```$ docker build -t <container-name> .```  
- ```docker build```: Build the container
- ```-t <container-name>```: Name the container
- ``` .```: Location of Dockerfile (current directory)  

#### List images
List built images to see that your docker image build  
```docker image ls```  

#### Running an image (creating the container)
```docker run -p 8080:8080 <image-name>```
- ```-p 8080:8080```: Forward port 8080 in the host (your computer) to 8080 in 
the container. So when your computer gets a requst to 8080, docker will forward
the request to :8080 in the container. We have specified in the docker file for 
our container to expose 8080, and our js file is listening on port 8080.



















