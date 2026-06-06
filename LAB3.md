Managing and Controlling Linux Services

(Based on: Linux Services Lab)

Session 1b: Exploring Linux Lab: Linux Services – Understanding and managing background services.

→ List services using systemctl list-units --type=service. These are the list of services

<img width="975" height="582" alt="image" src="https://github.com/user-attachments/assets/5d7691f1-318a-4afe-ab5b-f7dec3b24ba4" />


Checking the live status of a standard background network service such as the cron scheduler.


<img width="975" height="384" alt="image" src="https://github.com/user-attachments/assets/ae5c741a-ff58-4ecb-9f61-870d90febd0b" />

 
There was a warning of “The unit file, source configuration file or drop-ins of cron.services changed on disk. Run ‘systemctl daemon-reload’ to reload units”
I went on google and searched the meaning and realized that the system is telling me that “someone changed the configuration files for cron behind my back, and still running on the old version, You need to tell me to refresh.”
So I followed the instructions on the screen of systemctl daemon-reload. I googled this command as well and realized that it forces the system to scan the entire filesystem for modified configuration profiles and to update the system.

<img width="975" height="530" alt="image" src="https://github.com/user-attachments/assets/7ca4e94d-1f21-42ae-9e07-5e4245c60067" />


→ Start/stop services with sudo systemctl start|stop [service].
Tried to stop and restart the service, came across a warning "the unit file, source configuration file or drop ins of cron.service changed on disk, run "system-daemon reload" to reload units.
I did that and managed to stop the service alongside checking the status with "sudo systemctl status"
 
Tried to start the service again and checked status of services using "sudo systemctl status"
 

<img width="975" height="311" alt="image" src="https://github.com/user-attachments/assets/c1b77692-7d52-4728-9003-929c6c2e6910" />

