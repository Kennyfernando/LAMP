# **LAMP STACK PROJECT**
## L- Linux
## A- Apache
## M- Mysql
## P- Php

# **Preparing Requirements**
## AWS account setup and provisioning an ubuntus server
### Create, Download and Save your private key. This is usually saved in your Download folder as .pem file 
## Connecting to your Ec2 instance
### Copy the public ip address on your Ec2 instance created on your AWS account.
### On your computer terminal navigate to your download folder or any folder you have saved your private key file that was downloaded.
### When in the folder you can ssh into your Ec2 instance by running this command ***ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>***
### **NOTE** -Anywhere you see these anchor tags <>, it should be replaced with the value specific to your situation. Example, if the private key you downloaded was named **my-private-key.pem**, simply remove the anchor tags and insert **my-private-key.pem** in the command you are required to execute.

# **Installing Apache**
### Apache HTTP server is the most commonly used web server and right before installation you are adviced to update your server and then you can start your Apache installation.
***$ sudo apt update***
***$ sudo apt install apache2***
### After update and installation we run the below code to verify that apache2 is running as a service on our OS.
***$ sudo systemctl status apache2***

# **Installing MySQL**
### Mysql is a Database Management System that enables to store and manage data for your site in a relational database. To install Mysql and l we runn the below command.
$ ***sudo apt install mysql-server***
##
# **Installing PHP**
### After installation of Apache to serve your content and Mysql to store and manage your data. PHP is the component of our setup that will process code to display dynamic content to the end user. In additon to the PHP package, you'll need ***PHP-Mysql***, a PHP module that allows PHP to communicate with MySQL-based database. You'll also need ***libapache2-mod-php*** to enable Apache to handle PHP files. Core PHP packages will automatically be installed as dependencies. 
## To install these 3 packages at once, run:
***$ sudo apt install php libapache2-mod-php php-mysql***
## After installation we run the below command to confirm your PHP version
***$ php -v***