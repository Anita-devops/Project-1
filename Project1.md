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

![Apache-file7](./Images/Apache-file7.PNG)

 ### Logging into the MYSQL console

    `sudo mysql`

![Apache-file8](./Images/Apache-file8.PNG)

*setting password for the root user*

    `ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

![Apache-file9](./Images/Apache-file9.PNG)


*Exiting the MYSQL Shell*

    `mysql> exit`