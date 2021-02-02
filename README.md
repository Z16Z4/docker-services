# docker-services + nginx proxy


git clone <repo>

cd docker-services

cd proxy
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install docker -y (or follow docker installation guide)
sudo apt-get install docker-compose -y
sudo apt-get install vim -y
vim docker-compose.yml
edit configuration with password and username
enter, :wq!
docker-compose up -d
docker ps -a
(confirm proxy is up and external network is created)
cd ..
cd cloud
vim docker-compose.yml
change the lines for username and passwords
enter , :wq!
docker-compose up -d
cd ../minecraft
docker-compose up -d
docker inspect <container id> to get local Ip
then login to nginx proxy manager at 127.0.0.1
username : admin@example.com
password: changeme
(then change username)
add SSL and configure proxies using IPs from docker inspect 
either port forward and add them to your domain , or use VPS ip with domain. go to 192.168.0.1, or 192.168.1.1 / (check windows ipconfig, or ifconfig)
