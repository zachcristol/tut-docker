# Running docker image

We will be using a basic node image to run a simple JS server (/src/index.js)  

### Dockerfile

```
# What docker image to build on. Find this on hub.docker.com: https://goo.gl/m8GKco
FROM  node:10.14.2
# Specifies that the running docker image will expose the port :8080.
This is because our js app listens on port :8080
EXPOSE 8080
# Copy index.js into the root directory of the container
COPY src/index.js .
# Commands to be run when the container starts
CMD node index.js
```

