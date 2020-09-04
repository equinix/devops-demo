# NGNIX DEMO

## Build the docker file 
* Step 1:

`cd ../nginx_demo/`

* Step 2:

` docker build --rm -f "dockerfile" -t first-ng_tag . `

* Step 3: 

`docker run --name first-ng_tag  -p 80:80 -p 443:443 first-ng_tag`

## Test the newly created NGINX Server docker  

`http://localhost/site1/` this url should open the Site One content 

`http://localhost/site2/` this url should open the Site Two content 

`http://localhost/site3/` this url should open the Site Three content 

`http://localhost/site4/` this url should open the Site 4 content where you will see the API call demo content 

`http://localhost/api/v1/employees` this url will direct the call to fetch the data from an External API.


## WorkNote

if you face any issue running the above created Image, one reason could be the Tagname is already in Use.

to reuse the Tag name execute the below Commend

`docker system prune`

the Above Commend will clear up all the space occupied by old Images.