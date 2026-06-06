Lab: Digital Certificates – Use Let's Encrypt to secure a server. 

I firstly installed nginx with sudo apt install ginx -y and checked if it was successfully downloaded and active with sudo systemctl status nginx.


<img width="644" height="289" alt="image" src="https://github.com/user-attachments/assets/d6fa3d02-8c82-4b24-ac3c-c3a1b46d2821" />

<img width="726" height="238" alt="image" src="https://github.com/user-attachments/assets/3c849252-adc5-4de5-8090-91d87fb5821e" />

 
I then installed certbot with sudo apt install certbot python3-certbot-nginx -y

 <img width="623" height="295" alt="image" src="https://github.com/user-attachments/assets/0644ba9d-36ef-489b-98fe-647a92d9ec8e" />

I run sudo certbot –nginx -d kaixi-isea-lab.duckdns.org. Came across a error of Timeout during connect  (likely firewall problem) and googled a fix for it. 

Google told me the reason this happened was because my VM is fresh, Azure blocks public web traffic by default. 
Azure has firewall settings that are controlled by something called a Network Security Group. So to fix this I have to open Port 80 and Port 443 in Azure. 


<img width="975" height="396" alt="image" src="https://github.com/user-attachments/assets/ccee4072-54ea-41db-b908-4c6af90187ae" />

 
For Port 80 (HTTP Rule) I had to add a port rule on the Azure portal. I made changes in service to HTTP and ensured that the Action is set to Allow. 

 <img width="472" height="578" alt="image" src="https://github.com/user-attachments/assets/2ebdcb5c-fec0-4140-8b99-6507a5d6a439" />


For Port 443 (HTTPS Rule) I also added a port rule, changing the service to HTTPS.

<img width="434" height="619" alt="image" src="https://github.com/user-attachments/assets/7dd64f5f-1e99-45b8-8da9-89cd823cd4dc" />
 

After ensuring both of them have been added into the port rules, I ran sudo certbot –nginx -d kaixi-isea-lab.duckdns.org again and it successfully loaded the certificate.
 

<img width="975" height="298" alt="image" src="https://github.com/user-attachments/assets/6f25ee64-a9d8-4d49-9b0c-34c07efbe09a" />


I then checked on google if have obtained the certificate using my domain in browser.

<img width="975" height="405" alt="image" src="https://github.com/user-attachments/assets/1bd635c2-fdbc-488f-9c2f-efc27479a67b" />

 
I found that normal HTTP is risky because it transfers data without encryption. We utilize Certbot to transition to HTTPS, which encrypts all user-server connection. 
I first ran across a problem where a connection timeout caused the command to fail. I found that Azure's default filtering of public web traffic was the cause of issue. 
After I configured the port rules to allow HTTP and HTTPS traffic in the portal, the software worked perfectly.
