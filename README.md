# SnipeIT-Ansible
SnipeIT Installation on Ubuntu_Automated With Ansible

<h3>Snipe-IT is one of the open-source software for IT Assets Management that gives Transparency, security, and oversight to your IT assets.</h3>

1. Install Ubuntu Server 20.04

   Open SSH or Putty and first update and upgrade the packages by running below command
```
sudo apt update -y && sudo apt upgrade -y
```
2. Install LAMP (Linux, Apache, MySQL, PHP) on Ubuntu

   Install Apache2
Install apache2 by using below command
```
sudo apt install apache2 -y
```
    Now Enable and Start apache2 service
```
systemctl start apache2 && systemctl enable apache2
```
    Now check the status of the service
```
systemctl status apache2
```
    Let us now check the version of apache2 to validate
```
apache2 -v
```
    In case the firewall is enabled you need to open HTTP and HTTPS ports to this server. just run the below commands for the firewall.
```
sudo ufw allow 80/tcp

sudo ufw allow 443/tcp

sudo ufw reload
```
    Now you can open the browser and validate that the webserver is ready with apache2.
```
http://<serverip>
```
    Snipe-IT needs various extensions, let us enable one which is mandatory
```
sudo a2enmod rewrite
```
```
systemctl restart apache2
```
    Restart apache2 and move to the next step.

  Now let us install other packages.

  MySql / MariaDB
    This is the Database Server Installation. You need to first install the database Server and Client both will be installed using below command.

```
sudo apt install mariadb-server mariadb-client -y
```


