# JENKINS Demo

## JEnkins Installation using Docker.

#### Pre-requestes
* Docker for Windows or MAC is installed 
* Docker hub user id and password 
* Port 8080 should be free, if not change the port in below commend to something else.

### Install Jenkins

Create a folder with read/write Access


`mkdir /Users/<your_name>/jenkins_home`

once you create the folder use the below commend to run Jenkins docker image 

`docker run -v /Users/<your_name>/jenkins_home:/var/jenkins_home  -p 8080:8080 -p 50000:50000 jenkins/jenkins`

What this above commend does on your machine
when you execute the above commend the following will happen
* Download Latest Jenkins Docker image from DockerHub validating your User credentials
* run the Jenkins Docker Image on your local machine
* the `jenkins_home` directory will be mount inside the Jenkins container and start nstalling all required plugins 
* Start The Jenkins tool in 8080 port 

How to setup Jenkins

launch http://localhost:8080/

the url will prompt for Secret password, execute the below `cat` command and copy past the password and click continue

`cat /Users/<your_name>/jenkins_home/secrets/initialAdminPassword`

follow the Wizad to install required plugins. choose Selected Plugins (This may take about 15 minutes based on your internet Speed)

once Plugin installed the system will prompt for first Super Admin User info.
Keep the the default Instance Configuration.
your Jenkins is ready to use now!

## How to create your First Jenkins Job

* Step 1:

on Landing Page of Jenkins you will see the option to Create Job [Click](http://localhost:8080/newJob)

* Step 2:
 * Provide your Job Name
 * Select Freestyle project from the list
 * Cick OK Button floating on bottom Left corner.

* Step 3:
 * select Checkbox of GitHub Project and input your Forked Git Repository
 
 `https://github.com/<your_neme>/devops-demo.git`

 * Step 4:
 Add Build Execution and add the below Commands

 ```
 # to Stop the Existing running Container
docker stop nginx_web_server 

# to Remove and clean the Existing Image
docker rmi -f nginx_web_server

```

