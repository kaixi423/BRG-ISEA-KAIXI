Understanding and Applying Linux Permissions

(Based on: Linux Permissions Lab)

Lab: Linux Permissions – Explore and apply file and directory permissions.

→ Use ls -l to view permissions.
Created a quick script file to experiment the permissions on. Using "touch perm_test.sh" and also viewed the default permissions using "ls-1"

Here it showed -rw-rw-r--. r stands for read, w stands for write and x stands for execute. So -rw-rw-r-- means that this is a regular file that the owner and group can read and change but everyone else can only look at the file.


<img width="688" height="127" alt="image" src="https://github.com/user-attachments/assets/d1661456-efeb-4504-a164-b20a24aa3a27" />

 
→ Change permissions using chmod (e.g., chmod 755 file.sh).
Managed to change permissions from read and write only to read,write and execute using chmod u+x perm_test.sh

<img width="889" height="220" alt="image" src="https://github.com/user-attachments/assets/ca0fa9e9-7c4c-4e15-972f-eb2079d0b276" />

<img width="673" height="116" alt="image" src="https://github.com/user-attachments/assets/28acd6a4-e80a-4cee-bf73-a0d31d28fc92" />

 
→ Change ownership using chown user:group file.txt.
 

<img width="686" height="177" alt="image" src="https://github.com/user-attachments/assets/3310a804-e98c-4b17-9cc7-7d4e01e8b87b" />

I learned the difference between chown and chmod that chmod is changing mode which is used to modify what actions can be done to a file while chown modifies who owns the permissions. 
