# Metasploitable Hacking

## Objective

The Metasploitable Hacking project was aimed to use an intentially vulnerable framework to simulate penetration testing. The goal was to gain practical experience in identifying vulnerabilities such as weak passwords, outdated software, etc. This project deepened my understanding of essential penetration testing techniques and tools as well as the use of ethical hacking to help secure systems.

### Skills Learned

- Practical penetration testing using Metasploit framework
- Vulnerability scanning and threat analysis
- Exploitation of system vulnerabilities such as weak passwords
- Using ethical hacking tools for threat analysis
- Understanding of bind shells and reverse shells with respect to ethical hacking

### Tools Used

- NMAP used to conduct network analysis and port discovery
- Netcat used to establish reverse shells
- Metasploit framework used to exploit vulnerabilities
- Web Developer tools used to exploit http vulnerabilities

## Project Walkthrough
First, I installed a Metasploitable2 Virtual Machine, which is a system that is meant to be hackable to practice penetration testing. I also installed Kali Linux, which I would use to hack Metasploitable. 

*Ref 1: Metasploitable2 and Kali Linux VMs*

<img width="600" alt="Screenshot 2024-12-20 at 8 35 29 PM" src="https://github.com/user-attachments/assets/2872f5ed-4a01-4f79-b79c-b95bfaea9673" />

To begin, I scanned for general vulnerabilities and open ports using an NMAP command. I found multiple possible vulnerabilites, such as smtp, http, and vnc.

*Ref 2: Scanning for vulnerable ports*

<img width="600" alt="Screenshot 2024-12-20 at 7 33 28 PM" src="https://github.com/user-attachments/assets/3e07826d-9506-4fd9-8ef5-1b25427b3568" />

My first vulnerable server to exploit was smtp. I used a smtp vulnerability scanner using metasploit and was able to find sensitive information that a client would not want to be easily discoverable, such as a list of all users.

*Ref 3: SMTP exploit: List of users found*

<img width="600" alt="Screenshot 2024-12-19 at 4 09 51 PM" src="https://github.com/user-attachments/assets/7a236ad9-d9d0-4580-a7cc-e977e465f1c7" />

My next server to exploit was http. For this part, I used web developer tools on my browser to help hack my Metasploitable's website. I found out that the website uses PHP scripting, and this knowledge allowed me to find a php info file with lots of sensitive info to the website. I was also able to access a robots.txt file associated with the website, which eventually led me to access a passwords directory containing accounts and passwords, which should be unaccessable to the public. Then, on kali linux's metasploit, I was able to use an http exploiter to establish a reverse shell on the website and access all sorts of sensitive information.

*Ref 4: Website passwords directory*

<img width="600" alt="Screenshot 2024-12-19 at 5 18 16 PM" src="https://github.com/user-attachments/assets/c3a4964b-4df6-48fe-a6c1-edacbc99326e" />

*Ref 5: Establishsing reverse shell*

<img width="600" alt="Screenshot 2024-12-19 at 10 53 22 PM" src="https://github.com/user-attachments/assets/f400374b-cb2b-487d-89ed-b36158046212" />

My last server to exploit was VNC. I was able to hack into the VNC using a vnc_login scanner in metasploit. This scanner uses a long list of passwords and uses them to attempt to log in to the VNC. Because the password was not a strong one (it was 'password'), we were able to log in. This is obviously a situation that a client would want to avoid.

<img width="600" alt="Screenshot 2024-12-20 at 1 15 46 PM" src="https://github.com/user-attachments/assets/512c3a5b-9f84-4464-892a-cd3d399dd930" />










