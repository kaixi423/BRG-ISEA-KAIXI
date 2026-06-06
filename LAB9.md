Obtaining and Managing Digital Certificates with Let’s Encrypt
(Based on: SSL Certificate Lab)

Session 3a: DNS & Certificates 
Freenom completely shut down so I will be using another free alternative which is DuckDNS.


<img width="516" height="456" alt="image" src="https://github.com/user-attachments/assets/2a1f3915-1a5b-41ce-8f18-91a2a27f20e9" />


Created a domain via DuckDNS:
 

<img width="665" height="588" alt="image" src="https://github.com/user-attachments/assets/65010e1c-0f50-43ec-a5c5-60b460f61434" />

Configure a record to point to server public IP. I did not know what this meant and googled it and realized that “A record” is aa specific type of DNS setting. 
It’s sole job is to map a human-readable domain name to a computer-readable IP address. 

I then verified the DNS propagation.

I did not know what this meant and also googled it. I realized that it meant a period where after you make a change to your DNS settings. It is the time needed for routers or computers to access the globe to update the records with my IP address.

To verify the DNS using nslookup, I went back to Azure terminal and ran the command.
 
I was curious as to why I had “ ;; communications error to 127.0.0.53#53: timed out” for a second and had the result after so I went to google it. 
I learned that I experienced something called a DNS server fallback. The server tried to look into its own memory, but because it took too long to respond, it gave a error. 
However the system used its backup plan and skipped the local memory and asked the internet servers directly. Then the servers found the domain I used and produced the right results. 
