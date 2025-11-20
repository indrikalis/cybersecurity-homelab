# Ubuntu Server

Steps for the setup, and make sure the Ubuntu Server ISO file has been downloaded. 

## initial setup in virtual machine, here I use virtual box.

a. The first step is to set your lab name as you prefer, for example: indrilab.

<img width="500" height="572" alt="image" src="https://github.com/user-attachments/assets/cdb61ccc-fa89-480f-883a-932dfea4af6a" />

b. Add the Ubuntu ISO file to Controller: IDE in the Storage panel.

<img width="500" height="595" alt="image" src="https://github.com/user-attachments/assets/e71a78c0-94dc-4726-9353-4ae442fb0234" />

c. Set the network to Bridged Adapter so it can connect directly to your home router. And make sure the adapter name matches the one listed in your device’s network drivers.

<img width="500" height="577" alt="image" src="https://github.com/user-attachments/assets/7dc6fa3e-b2a6-4cf5-9282-93a47068f5e8" />

If everything looks correct, you can proceed to run your VM.


## Set up during the installation.
a. Here you will find a form for the username and password. As an example, please refer to the image.

<img width="500" height="786" alt="image" src="https://github.com/user-attachments/assets/a3bef895-a9f5-4204-a267-70f6a657f304" />

b. Next, there is an option for SSH to enable remote server access; please just check the box.

<img width="500" height="798" alt="image" src="https://github.com/user-attachments/assets/9006aba9-454e-4951-a74c-de4ba41f645e" />

c. Once the installation process is complete, the initial screen will look like this.

<img width="500" height="757" alt="image" src="https://github.com/user-attachments/assets/30c91613-738b-4172-8432-e7a5ab63725c" />

## Setup and installation of the target environment..
a. 	Update & upgrade system 
```bash
1.	sudo apt update && sudo apt upgrade -y
2.	sudo apt install net-tools curl wget unzip -y
```
b. Install the common target services.
1. Apache Web Server + PHP 
```bash
1.sudo apt install apache2 php libapache2-mod-php php-mysql -y
2. sudo systemctl enable apache2
3. sudo systemctl start apache2 
```
Once done, we can check using the command 
```bash
sudo systemctl status apache2.
```
<img width="500" height="734" alt="image" src="https://github.com/user-attachments/assets/f9fa93c5-a6f4-4a79-a8ad-4f8be68dc06d" />

Akses from host browser : http://IP_Ubuntu

If the installation is successful, the result will look like the following:

<img width="500" height="699" alt="image" src="https://github.com/user-attachments/assets/d2ad8e22-76e0-4cc8-97ca-808c02e12405" />

2. Databse server
Update Sistem
```bash
sudo apt update
```
Install MySQL Server
```bash
sudo apt install mysql-server -y
```
Cek Status MySQL
```bash
sudo systemctl status mysql
```
<img width="500" height="510" alt="image" src="https://github.com/user-attachments/assets/a8192429-c1b3-4a55-8bb4-7a27642f5427" />


















