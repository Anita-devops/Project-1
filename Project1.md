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