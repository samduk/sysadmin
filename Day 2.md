# Input Validation 


function test_input($data){
    $data = trim($data);   
    $data = stripslashes($data);  ###xss
    $data = htmlspecialchars($data);  ###xss
    return $data;

}


List of Super Globals 

$_REQUEST (both POST and GET)

## My Question 
    Can we enforce password type in mysql + Salted password (Salt )  ?
    SSL certificate for medium size company ?
    SSLstrip 
vaultpress 

# WordPress Install 


# Prerequisite 
    -   ~~~PHP~~~
    - Database Name : wordpress
    - Database Username : wpuser
    - Password : password
    - Host : localhost


# To Download

    - ```wget https://wordpress.org/latest.tar.gz```


# Issues 
    Conflict with 192.168.56.101 BWA with Ubuntu Web Server 

# Steps
    - wget https://wordpress.org/latest.tar.gz
    - tar -xzvf latest.tar.gz
    - sudo rm /var/www/html/*
    - sudo cp wordpress/* /var/www/html -R   ##### Need to be careful if you require a separate folder 

    ## Database setup 

    - create database wordpress;
    - create user "wpuser"@"localhost" identified by "Password";
    - grant all on wordpress.* to "wpuser"@"localhost"; 
    - flush privileges;
    - exit 

    ## Configure WordPress

    -   sudo nano wp-config.php 
    -   copy the content from web 

    ## WordPress Website Credentials 

    -   username: admin_tcrc 
    -   password: I4RZMlNm4^A)tq)NbU

    - https://wordpress.org/plugins/classic-editor/ 

- SCP is good to use File Transfer, sepcially when you need to exchanges files or filders between your computer and server

________________________________

## Port Forwarding 

-   [Reading](https://help.ubuntu.com/community/SSH/OpenSSH/PortForwarding) ***


- sudo ssh researcher@192.168.56.101 -L 8000:192.168.56.101:80 

- For window user: use PuTTy use SSH Tunneling 

***
### Fixed FTP credential asking 

```sudo chown username:www-data /var/www -R```

```sudo chmod g+w /var/www -R```

***

## 
```sudo netstat -antp``

## Resource link

- [codex](https://codex.wordpress.org) 
- [developer](https://developer.wordpress.org) 
- [youtube resource](https://www.youtube.com/watch?v=0l7JTie_6jM&list=PLriKzYyLb28kR_CPMz8uierDWC2y3znI2) ***

***
## Cyber Security Practices 

#### [The Cyber Security Framework](https://www.nist.gov/cyberframework) 
    -   Identify  
    -   Protect 
    -   Detect
    -   Respond 
    -   Recover

***
End of the day 02 

### Note: Kindly note that the username and password mentioned there is dummy and not using. Provided you have concerns of this post. :) 






























