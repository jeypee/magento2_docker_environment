# PHP 7, Apache, MySQL (LAMP) docker environment
Docker container with php 7 on Apache (httpd) MySQL and all Magento2 dependencies declared. Based on an docker-compose.yml file.

| System  | Version | Comment  |
|---------|---------|----------|
| Mysql   | 5.7.21  |  			 |
| PHP     | 7.0.16  |   		 |
| Apache  | 2.4.10  |   		 |



# Requirements
- Docker (Virtualbox installed with docker)
- Magento 2 installer source. Go to [https://magento.com/tech-resources/download]()  

# Run project

## Environment setting-up
- browse into `cd magento2_docker_environment`
- for convenience edit your **/etc/host** with your favorit text editor and add a localhost route: `127.0.0.1 host1.local`
- Type in the docker terminal: `docker-compose build`
- Type in the docker terminal: `docker-compose up -d`

## Magento 2 installation
- copy Magento 2 installer source into **sites** folder
- open your browser and go to: `http://host1.local/`
- select Magento 2 site and follow the installation guide. 
- after that your able to use your new Magento 2 market place

# Settings

You can add more `Virtual Hosts` in `etc/apache2/hosts.conf` the host1.local is in there.

Database name (DDL script must be updated in this case) and password are located in `docker-compose.yml`.

All scripts for creating databases must be located into **etc/mysql/init** folder
