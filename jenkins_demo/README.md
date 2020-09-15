# JENKINS Demo

## Jenkins Installation & Setup using Docker.
 Follow instruction in this Document: [Jenkins-Install-Step-by-Step-Guide.docx](Jenkins-Install-Step-by-Step-Guide.docx)

 ### demo Project we use for this Demo
 `https://github.com/equinix/devops-demo.git`

 ```
echo "Build Started"

docker stop nginx_web_server 

docker rmi -f nginx_web_server

pwd

ls -al 

cd nginx_demo

docker build --rm -f "dockerfile" -t nginx_web_server .

docker run -d --name nginx_web_server  -p 80:80 -p 443:443 nginx_web_server
```

