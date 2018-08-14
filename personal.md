# Personal Documentation 
***
### Setup LAMP (Secure Approach)
- Server OS : uBuntu 16.04.5
    #### Credentials of your server
    - Take down the Host Name
    - Username
    - Password 
- Choose LAMP 
- Open SSH 
- Standard System Utilities
    #### Credentials of your MySql Database
    - Take down the password 

### HTOP 
~~~I used this command to monitor server~~~

```sudo apt-get install htop```


### Enabling SSH Access 
- Enable Host Only Adapter 
- ```sudo nano /etc/network/interfaces```
- ~~~add auto infront of the adapter~~~

### Hardening SSH 



***
## How to secure mysql server 
***
Script to create a directory layout for our databases 

```sudo mysql_install_db```  ### This code is deprecated

Remove some defaults that are dangerous to use in a production environment 

```sudo mysql_secure_installation```

### Security Through the ```My.conf``` File 

- Main configuration file for MySQL  is ```my.conf```file located in the ```/etc/mysql``` directory on Ubuntu and the "/etc/" directory on some other VPS. 

    - ```sudo nano /etc/mysql/my.conf``` ###

        - ```bind-address``` setting within the [mysqld] section should be set to... 

        - ```bind-address = 127.0.0.1```
    
        ~~~This makes sure that MySQL is not accepting connections from anywhere except for the local machine.~~~

    - ```local-infile = 0 ```
    ~~~In the same section of the file; Should be closed unless you absolutely require it.~~~
    ~~~Add the directive to disable ability to load local files~~~
    ~~~This will disable loading files from the filesystem for users without file level privileges to the database~~~

    - ```log=/var/log/mysql-logfile```
    - ```sudo ls -l /var/log/mysql*```

    ~~~Make sure MySQL log, error log, and mysql log directory are not readable by other user.~~~

### Securing MySQL From Within 

```mysql -u root -p```
### Securing Passwords and Host Associations

```SELECT User, Host, Password FROM mysql.user```

~~~Make sure there are no users without a password or a host association in MySQL~~~

```UPDATE mysql.user SET Password=PASSWORD('newPassword') WHERE User="demo-user";```

~~~to change "%" (which is a wildcard that means any host.) to localhost ~~~

```UPDATE mysql.user SET host = 'localhost' WHERE User="demo-user";```

~~~To remove blan users~~~

```DELETE FROM mysql.user WHERE User="";```

```FLUSH PRIVILEGES;```

***




