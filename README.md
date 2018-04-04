# Web-Server-Team
Linux Star is our team name.


Team Name: Server squad?

Research: Chinou
Hosting a web server we using apache2 to make a server host. 

Web server is a program that uses HTTP(Hypertext transfer protocol) to serue the file from web pages, in response to the request which one forward by their computes HTTP clients.

Web servers have plugins to support scripting languages like perl, PHP, ASP, JSP
Example; Apache tomcat, microsoft’s internet information server, Nginx, google web server.


-HTTP(Hypertext transfer protocol) is a well known protocol used in web servers. HTTP is responsible for answering and responding to incoming requests.

-Php is a language that is used to develop static or dynamic websites.  PHP uses a mix of interpretation and compilation to provide the best combination of performance and flexibility for developers



-Apache Software exists to provide robust and commercial-grade reference implementations of many types of software. It must remain a platform upon which individuals and institutions can build reliable systems, both for experimental purposes and for mission-critical purposes.

Types of Web servers:
A dynamic web server consists of a static web server plus extra software, most commonly an application server
A static web server, or stack, consists of a computer (hardware) with an HTTP server (software). We call it "static" because the server sends its hosted files "as-is" to your browser
Documentation: Shue 
Setting Up Your Own Web Server:
Installing Apache:
In console window, type: sudo apt-get update and type in your root password
sudo apt-get install apache2
Confirm with y and ENTER
Test with sudo apache2ctl configtest  
If you get error: domain name not set, edit configuration file sudo nano /etc/apache2/apache2.conf scroll to bottom and add: ServerName 127.0.0.1 then save and quit with CTRL O CTRL X
Test again, should get syntax ok message
Reboot to finish install: sudo systemctl restart apache2
Then open web browser, type in localhost.0.0.1 site will display showing install is working ok
Go to your file explorer root folder and open index.html folder to allow mods: sudo chmod 777 /var/www/html
Install MySQL:
sudo apt-get install mysql-server
Confirm with y and ENTER
Enter new root account and password for MySQL (different from normal root)
Optional: run security c
heck sudo mysql_secure_installation
Install php:
sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql  
(if you unable to do the command above try:  sudo add-apt-repository universe after this command do sudo apt-get update , the command above should work now)
ENTER
y and ENTER
Configure to prioritize php over html files
Open Apache config: sudo nano /etc/apache2/mods-enabled/dir.conf
On the second text line: add index.php before index.html, then delete index.php at the end of the line
Save and exit: CTRL O CTRL X
Finalize: sudo systemctl restart apache2
Go to html folder and create folder index.php
()
Open and add: <?php phpinfo(): ?>
Refresh browser; should display info about your version of Apache (if it doesn’t, exit and clear history, try again)
Install myadmin:
sudo apt-get install phpmyadmin
y and ENTER
Select apache2 and ENTER
Then type MySQL password and confirm
ENTER
Finalize:
Confirm Apache config file sudo nano /etc/apache2/apache2.conf
Scroll down to end and do Include /etc/phpmyadmin/apache.conf
CTRL O CTRL X
Restart: sudo systemctl restart apache2
Type in web browser localhost/php/myadmin
Should be able to log in with root account and password, to edit the database


Testing: Kong Meng
-How to edit the website

Hey this is a website that shows you more in depth about how to create our own web servers https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04 (Chinou)

This video is also really helpful https://www.youtube.com/watch?v=avEDRh8gGGY&t=86s









Support: Mussie

Web servers can be either a software unit or a hardware unit, which provides the web pages via HTTP. Web server gets the request and fined the resources then response to client. The files stored on web server are ready by browsers, such as Google Chrome, Safari, Internet Explorer, and Firefox. During using thoughts browser, it communicates with web servers to bring us information from internet. Web server can communicates with numerous browsers at the same time on computers. Through delivery of web pages, web servers follow a network protocol is called HTTP. HTTP is hypertext transfer protocol and it serve the files that form Web pages to users, in response to their requests. Web servers are functioning with Linux or Microsoft Windows. Most web servers today operate Linux and also most websites are hosted on Linux servers.
Upload_files_to_a_web_server
https://www.youtube.com/watch?v=-q8Jj4aAWYw





