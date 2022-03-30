# Docker-Task
1- install Docker & Docker Compose on my machine 
2- then i create directory contain three files :
       - php.Dockerfile 
       - docker-compose.yml
       - html 
3- for the php.Dockerfile :
    -This is a Dockerfile which enables mysqli and PDO php extensions in the php:7.4.3-apache image from Docker Hub and builds a custom Docker image from it.
4- for the docker-compose.yml : 
    -I have created 3 services web-server, mysql-server and phpmyadmin.
5- html :
    -it contain my php code.
6- docker-compose.yml explain :
   - web-server service will run a custom-built Docker image as defined in php.Dockerfile.
   - mysql-server service will run the mysql:8.0.19 image (from DockerHub) in a Docker container.
   - phpmyadmin service will run the phpmyadmin/phpmyadmin:5.0.1 image (from DockerHub) in another Docker container.
   - In mysql-server service, the MYSQL_ROOT_PASSWORD environment variable is used to set the root password of MySQL.
   - In phpmyadmin service, the PMA_HOST, PMA_USER, PMA_PASSWORD environment variables are used to set the MySQL hostname, username and password respectively      that phpMyAdmin will use to connect to the MySQL database server running as mysql-server service
   - In mysql-server service, all the contents of the /var/lib/mysql directory will be saved permanently in the mysql-data volume.
   - In the web-server service, the container port 80 (right) is mapped to the Docker host port 8080
   - In the phpmyadmin service, the container port 5000 (right) is mapped to the Docker host port 80
7- start the web-server, mysql-server and phpmyadmin services, run the following command:
   - $ docker-compose up -d
8- Testing the LAMP Server :
   - test phpMyAdmin by using any browser in virtual machine network by using the following url : http://192.168.182.128:5000
   - to access webserver using the following url :  http://192.168.182.128:8080
   - 



