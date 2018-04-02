# PHP 7, Apache, MySQL (LAMP) docker environment
Docker container with php 7 on Apache (httpd) MySQL and Magento2 provided. Based on an docker-compose.yml file.

| System  | Version | Comment  |
|---------|---------|----------|
| Mysql   | 5.7.21  |  			 |
| PHP     | 7.0.16  |   		 |
| Apache  | 2.4.10  |   		 |
| Magento | 2.2.3   | Community edition |



# Requirements
- Docker (Virtualbox installed with docker)

Go to your terminal and Clone or fork the project.

# Run project

- browse into `cd magento2_docker_environment`
- for convenience edit your **/etc/host** with your favorit text editor 
- `sudo vi /etc/hosts`
- add or replace IP with your docker IP: `192.168.99.100 host1.local`
- Type in the docker terminal: `docker-compose build`
- Type in the docker terminal: `docker-compose up -d`

Now open your browser and go to: `http://host1.local/`
in your browser you should see a PHP 7 info page. 

# Settings

You can add more `Virtual Hosts` in `etc/apache2/hosts.conf` the host1.local is in there.

Database name and password are located `docker-compose.yml`.

All scripts for creating databases are located into **etc/mysql/init** folder
