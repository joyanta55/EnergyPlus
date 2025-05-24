Dockerfile
-------
**Pre-requisite** Make sure your docker runs in rootless mode. If you can run 
```
docker run hello-world
```
 without sudo, you are good to go. 

Create Dockerfile rules to export energyPlus. Run the following command to build the docker image
```
    docker build --no-cache -t energyplus .
```

To test

```
    docker run energyplus -h
```
