# Installation and setup method for DVWA
The main function of DVWA (Damn Vulnerable Web Application) is to serve as a deliberately insecure platform (full of vulnerabilities) for the purpose of learning and training in web security (penetration testing).
## First, we are going to create the database for the DVWA user in MYSQL.
Follow the following commands and adjust them according to your preference, such as the username and password.
1. Enter MySQL.
```bash
CREATE DATABASE dvwa;
```
2. Create DVWA user.
```bash
CREATE USER 'dvwa'@'localhost' IDENTIFIED BY 'p@ssw0rd';
```
Adjust the username and password that you want to use.

3. Database Permission Management.
```bash
GRANT ALL PRIVILEGES ON dvwa.* TO 'dvwa'@'localhost';
```
4. Reload and update the permission tables inside the MySQL server.
```bash
FLUSH PRIVILEGES;
```
5. exit
```bash
exit;
```
## Next Step: Installing DVWA
1. Follow the following command(s).
```bash
sudo wget https://github.com/digininja/DVWA/archive/master.zip
```
```bash
sudo unzip master.zip 
```
```bash
sudo mv DVWA-master dvwa 
```
```bash
sudo rm master.zip
```
2. Copy config sample
```bash
cd dvwa/config
sudo cp config.inc.php.dist config.inc.php
```
3. Edit the config file (adjust it to match what is inside the database server).
```bash
sudo nano config.inc.php
```
<img width="500" height="480" alt="image" src="https://github.com/user-attachments/assets/caaf2a3f-e87d-4ea1-a63b-0dc7e5ca9372" />

4. Set the permission (important!).

```bash
sudo chown -R www-data:www-data /var/www/html/dvwa
sudo chmod -R 755 /var/www/html/dvwa
sudo systemctl restart apache2
```
After everything is successful, we will now access it using our browser. Access it at the URL (ip_ubuntu/dvwa).
If you installed DVWA on an Ubuntu Virtual Machine (VM), you must first determine the VM's internal IP address.

In your Ubuntu terminal, run the command: ip a or ifconfig

Look for the IP address (e.g., 192.168.1.100).

Open the web browser on your host machine (Windows/Mac) or directly on the Ubuntu VM, and enter the URL:
```bash
http://[Your_Ubuntu_IP_Address]/DVWA/setup.php
```
<img width="500" height="469" alt="image" src="https://github.com/user-attachments/assets/40424ca6-8d3d-49d3-85f6-c23031e4e194" />

DVWA credentials username: admin password: password.

## After logging in, the next step is to set up DVWA.
1. Click Create / Reset Database button
<img width="500" height="468" alt="image" src="https://github.com/user-attachments/assets/1e3dd792-0cf7-4eef-898b-9d2ce1215c06" />

If all configurations run well, the result will be as shown above. Good luck trying!





