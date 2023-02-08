## Detailed Documentation of Project 1
### Installing Apache and Updating Firewall

*update a list of packages in package manager*

	`sudo apt update`

![Apache-file1](./Images/Apache-file1.PNG)
![Apache-file2](./Images/Apache-file2.PNG)
    
*run apache2 package installation*

    `sudo apt install apache2`

![Apache-file3](./Images/Apache-file3.PNG)

*To verify that apache2 is running as a Service in our OS, use following command*

    `sudo systemctl status apache2`

![Apache-file4](./Images/Apache-file4.PNG)

    
**Testing how Apache HTTP server can respond to requests from the Internet**

[URL to launch](http://34.207.253.203:80)

![Apache-file5](./Images/Apache-file5.PNG)


*retrieving your Public IP address through the terminal*

![Apache-file6](./Images/Apache-file6.PNG)


### INSTALLING MYSQL

    `sudo apt install mysql-server`

![Mysql-file1](./Images/Mysql-file1.PNG)

 ### Logging into the MYSQL console

    `sudo mysql`

![Mysql-file2](./Images/Mysql-file2.PNG)

*setting password for the root user*

    `ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

![Mysql-file3](./Images/Mysql-file3.PNG)


*Exiting the MYSQL Shell*

    `exit`

![Mysql-file4](./Images/Mysql-file4.PNG)



*Starting the interactive script*

    `sudo mysql_secure_installation`

![Mysql-file5](./Images/Mysql-file5.PNG)
![Mysql-file6](./Images/Mysql-file6.PNG)
![Mysql-file7](./Images/Mysql-file7.PNG)


*Log in test into MYSQL Console*

    `sudo mysql -p`

![Mysql-file8](./Images/Mysql-file8.PNG)


*Exiting the MYSQL Console*

    `exit`
    
![Mysql-file9](./Images/Mysql-file9.PNG)


### INSTALLING PHP

    `sudo apt install php libapache2-mod-php php-mysql`

![PHP-file1](./Images/PHP-file1.PNG)


*Confirming the PHP version*

    `php -v`

![PHP-file2](./Images/PHP-file2.PNG)


### CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE
**Setting up PROJECTLAMP Domain**
*Creating the directory for projectlamp using ‘mkdir’*
    `sudo mkdir /var/www/projectlamp`
    `sudo chown -R $USER:$USER /var/www/projectlamp`
*creating and opening a new configuration file in Apache’s sites-available directory*  
    `sudo vi /etc/apache2/sites-available/projectlamp.conf`
*Enabling the new virtualhost*
    `sudo a2ensite projectlamp`
*disabling Apache’s default website*
    `sudo a2dissite 000-default`
*making sure your configuration file doesn’t contain syntax errors*
    `sudo apache2ctl configtest`
*reloading Apache so changes take effect*
    `sudo systemctl reload apache2`
*Creating an index.html file in location*
    `sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`
    
![Projectlamp-status1](./Images/Projectlamp-status1.PNG)

*Opening the created website URL using IP address on a browser*
[The new website using IP](http://34.207.253.203/)

*Opening the created website URL using public DNS name on a browser*
[using public DNS name](http://ec2-34-207-253-203.compute-1.amazonaws.com/)