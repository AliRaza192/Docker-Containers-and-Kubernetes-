# Docker CLI cheat sheet Management

### display system information
```docker info``` 

### display the system's version
```docker version``` 

### Log into a Docker registry
```docker login``` 


# Docker CLI cheat sheet Running and Stopping

### Log into a Docker registry

### Pull an image from a registry
```docker pull [imageName]``` 

### Run containers
```docker run [imageName]``` 

### Detached Mode
```docker run -d [imageName]```

### Start containers
```docker start [containerName]``` 

### List running containers
```docker ps``` 

### List all running and stopped containers
```docker ps -a``` 

### Stop containers
```docker stop [containerName]``` 

### Kill containers
```docker kill [containerName]``` 

### Get image info
```docker image inspect [containerName]``` 



# Docker CLI cheat sheet - Limits

### Max memory
```docker run --memory="256" nginx``` 

### Max CPU
```docker run --cpus=".5" nginx``` 



# Docker CLI cheat sheet - Attach Shell

### Attach Shell
```docker run -it nginx -- /bin/bash```

### Attach PowerShell
```docker run -it -- microsoft/powershell:nanoserver pwsg.exe```

### Attach to a Running Container
```docker container exec -it [containerName] -- bash```



# Docker CLI cheat sheet - Cleaning up

### Removes stopped containers
```docker rm [containerName]```

### Removes all stopped containers
```docker rm $(docker ps -a -q)```

### Images list
```docker images```

### Deletes the image
```docker rmi [imagesName]```

### Removes all images not in use by any containers
```docker system prune -a```



# Docker CLI cheat sheet - Building

### Builds an image using a Dockerfile located in the same folder
```docker build -t [name:tag] . ```

### Builds an image using a Dockerfile located in a different folder
```docker build -t [name:tag] -f [fileName]```

### Tag an existing image
```docker tag [imageName] [name:tag]```



# Volumes cheat sheet 

### Create a new volume
```docker create volume [volumeName]```

### List the volumes
```docker volume ls```
 
--name voltest is instance name -v my-vol is volume name and :/app is local folder
```docker run -d --name voltest -v my-vol:/app nginx:latest```

### Connect to our running instance
```docker exec -it voltest```

### Create a file in the volume using Nano
```apt-get update```
```apt-get install nano```

### Create a file in the app folder
```cd app```
```nano test.txt```

### O save file, X exit
```CTRL + O```
```CTRL + x```

### Inter in test.txt file
```cat test.txt```

### Display the volume info
vo```docker volume inspect '[volumeName]```

### Stop and remove the container
```docker stop [instanceName for example voltest]```
```docker rm [instanceName for example voltest]```

### Deletes a volume
```docker volume rm '[volumeName]```

### Deletes all volumes not mounted
```docker volume prune```

### CleanUp
```docker volume rm [instanceName for example voltest]```
```docker volume stop [instanceName for example voltest]```
```docker rm [instanceName for example voltest]```



# Docker Compose Cheat Sheet 

### Build the images
```docker compose build```

### YAML file located in anothers folder use -f and file location
```docker compose build -f [location]```

### Start the containers
```docker compose start```

### Stop the containers
```docker compose stop```

### Build and start
```docker compose up -d```

### List what's running
```docker compose ps```

### Remove from memory
```docker compose rm```

### Stop and remove
```docker compose down```

### Get the logs
```docker compose logs```

### Rund a command in a container
```docker compose exec [container] bash```


# Compose V2 - New Commands
### Rund a instance as a project
```docker compose --project-name test1 up -d```
### ShortCut
```docker compose --project-name test1 up -d```

### List running projects
```docker compose ls```

### Copy file from container
```docker compose cp [containerID]:[SRC_Path] [DEST_Path]```

### Copy file to the container
```docker compose cp [SRC_Path] [containerID]:[DEST_Path]```


# Push an image to Docker Hub

### Build the image
```docker build -t <yourDockerHubRegistryName>/<imageName> ```

### Push the image
```docker push <yourDockerHubRegistryName>/<imageName> ```

### Remove the local image
```docker rmi <yourDockerHubRegistryName>/<imageName> ```

### Pull the image
```docker pull <yourDockerHubRegistryName>/<imageName> ```

### CleanUp
```docker rmi <yourDockerHubRegistryName>/<imageName> ```




