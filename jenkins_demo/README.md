# JENKINS Demo

## Jenkins Installation & Setup using Docker.
 Follow instruction in this Document: [Jenkins-Install-Step-by-Step-Guide.docx](Jenkins-Install-Step-by-Step-Guide.docx)

 ### demo Project we use for this Demo
 `https://github.com/equinix/devops-demo.git`

 ```
echo "Build Started"

# to Stop the Existing running Container
docker stop nginx_web_server 

# to Remove and clean the Existing Image
docker rmi -f nginx_web_server

pwd

ls -al 

# CD into the project Folder
cd nginx_demo

# To Build the Docker image
docker build --rm -f "dockerfile" -t nginx_web_server .

#To Run the Docker Image 
# -d or  --detach -p or --publish
docker run -d --name nginx_web_server  -p 80:80 -p 443:443 nginx_web_server
```

