# FTPAnonChecker
Checks a large amount of FTP servers for anonymous login

First, run NMAP against the environment NMAP -p21 156.8.0.0/16 > ftp.txt
Then, grep out all the IPs of servers that has FTP in the OPEN state: cat ftp.txt | grep -B4 "open" > ftp-IPs.txt
Then run the FTPAnonChecker.py and point it to the ftp-IPs.txt file
The script will run through the IPs and color code the responses - green means anon login allowed - screenshot below
![image](https://github.com/user-attachments/assets/f9c2c83c-1f42-4b99-b0a2-08ce4da2c3fb)
