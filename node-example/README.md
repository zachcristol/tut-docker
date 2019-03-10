# Running docker image

We will be using a basic node image to run a simple JS server (/src/index.js)  

### Dockerfile

```
FROM  node:10.14.2
EXPOSE 8080
COPY src/index.js .
CMD node index.js
```

