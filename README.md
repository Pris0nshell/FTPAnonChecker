# FTPAnonChecker
Checks a large amount of FTP servers for anonymous login

First, run NMAP against the environment NMAP -p21 156.8.0.0/16 > ftp.txt
Then, grep out all the IPs of servers that has FTP in the OPEN state: cat ftp.txt | grep -B4 "open" > ftp-IPs.txt
Then run the FTPAnonChecker.py and point it to the ftp-IPs.txt file
The script will run through the IPs and color code the responses - green means anon login allowed - screenshot below
![image](https://github.com/user-attachments/assets/534ce649-652e-497d-9c6d-c503776b3be3)

