DOCKER: 


Some Docker commands: 
docker pull <image> ---> Used to pull images from repository
docker port <container id> ---> Used to identify the ports mapped to the container id
docker container inspect --format '{{ .NetworkSettings.IPAddress }}' <CONTAINER_NAME> ---> used to tell you the specific ip your docker container is using to communicate with the local host
docker network ls ---> used to show the containers and their network type
docker ps ---> Used to display the running containers and their id
docker ps -a ---> used to display the containers includng those hidden and their id 
docker images ---> used to display the images in a container
docker logs <container id> ---> Used to obtain logs for docker 
docker run --publish 8080:80 <service> ---> used to run a docker container and map it to port 8080 of your vm

docker run -p 3306:3306 -d --name mysql mysql/mysql-server:latest ---> used to run and obtain a hash for mysql database 

docker exec -it mysql bash ---> Used to bypass the ssh protocol (Docker does not make use of traditional protocols). log into the vm to maybe install a software
mysql -uroot -p ---> Used to log into mysql database itself. This is specific for databases. 
show databases; ---> Used to show databases
ALTER USER 'root'@'localhost' IDENTIFIED BY 'newpassword'; ---> Used to change the password to "newpassword"
create database weekly_product_sales; ---> query used to create a new database called "weekly_product_sales"
create database company_payroll; ---> query used to create a new database called "company_payroll"

docker commit <container id> --->  creates a copy of the running container in an image format. ie create an new image of that container (Container id can be obtained from docker ps)

docker tag <IMAGE ID> mysql/mysql-server/added-two-databases:v2 ---> This would allow you to tag specific images in your environment and label it v2

docker run -p 3310:3306 -d --name mysql-v2 mysql/mysql-server/added-two-databases:v2 ---> Update the port, version and repo name

docker exec -it mysql-v2 bash ---> log into the new mysql-v2 container









