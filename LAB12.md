Additional Server Service (Self-Selected)
(E.g., MariaDB, Docker, Nextcloud, VPN, etc.)

I will be choosing download MariaDB. To download MariaDB on my VM I ran sudo apt install mariadb-server -y

 <img width="975" height="463" alt="image" src="https://github.com/user-attachments/assets/79642bdc-5ec7-4e23-82a8-b93e64657725" />

I then verified that the service was running with sudo systemctl status mariadb 

<img width="975" height="429" alt="image" src="https://github.com/user-attachments/assets/b2291ee2-5ab8-47b2-bc0c-34ef04805ace" />

I then checked if MariaDB was functioning with sudo mariadb and chose to run a test SQL query to display the databases. I used SHOW DATABASES;  

 <img width="975" height="257" alt="image" src="https://github.com/user-attachments/assets/5490fb0e-551b-4b05-9d44-5746c3db8c06" />

<img width="472" height="347" alt="image" src="https://github.com/user-attachments/assets/bcb03aa9-10aa-4c86-bef8-7be1772e9476" />

This shows the basic functionality of MariaDB is working. 
I learned from this lab that websites and apps need a database service to ensure that it can store user data. This lab helped me understand how to install, secure and test a new server service on my own using the linux knowledge I have gained. 
