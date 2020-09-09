# Some Useful Docker Commands

```
#Start Ngnix web server using Docker
docker run --detach --publish 80:80 --name webserver nginx

#Stop Container
docker container stop <cont_name | cont_id> 

#Remove Container
docker container rm <cont_name | cont_id> 

#List all Running Containers
docker ps
or 
docker container ls

#List all Stopped Containers
docker ps -a
or 
docker container ls -a --filter status=exited --filter status=created

# see log in container
docker logs <cont_name | cont_id>

# clear or remove all Stopped Containers
docker container prune

# Clear of freeup diskspace
docker system prune

# log into running Container
 docker exec -it <cont_name | cont_id> bash

#List all available Images
docker images

#Remove Docker Image
docker rmi IMAGE_ID

#Inspect a Docker Image
docker inspect IMAGE_ID 

```