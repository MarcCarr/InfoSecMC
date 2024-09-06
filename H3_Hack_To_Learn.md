# Disobey - Cybersecurity in the Gaming Industry - Massimo Nardone
https://www.youtube.com/watch?v=85J8OJmwkbI

- The gaming industry involves billions of people, and circulates massive amounts of money annually, which is why cyber security is an integral part of the grand scheme.

- Multiplayer and online games are the most popular globally. Players can harmfully be affected by:
   - DDoS
   - Data security breaches
   - In-game transaction failure

- Game developers spend countless hours developing their games, and they need assurance their hard work is protected from:
   - Intellectual property theft
   - Game infrastructure exploitation

- Robust protection can be achieved by using, and fully understanding a suitable cyber security architecture.
- Utilising the secure software development life cycle (SSDLC) process can mitigate potential vulnerabilities, and create a framework of best practices to follow.
   - SSDLC includes: Training -> Requirements -> Design -> Implementation -> Verification -> Release -> Response
- Industry standards, frameworks, and regulations promote cyber security.
   - GDPR in Europe
   - PCI DSS for secure transactions.

- Individual players can account for a good amount of security in gaming by following basic cyber security practices like account and password management.
-


# Karvinen 2020: Command Line Basics Revisited
https://terokarvinen.com/2020/command-line-basics-revisited/

- As the name suggests, Command Line Basics Revisited is a concise collection of Linux command line inputs for standard usable situations.
- This covers basics from navigating your machines directory to updating or installing software.

- Every example is clearly explained with the added help of key placement on your keyboard.
- Space, and key usage tips are a great attribute as command line is not always clear.


# Bandit oh-five
https://overthewire.org/wargames/bandit/

Level 0 -> 1
   - I opened the terminal in VM where I conneced to SSH bandit.labs.overthewire.org by writing bandit0@bandit.labs.overthewire.org -p 2220 (-p 2220 specifies port number 2220)
   - I entered the provided password and was granted access.
   - Once in, I used 'ls' to see files in current directory -> cat readme to find password for next level.

Level 1 -> 2
   - I opened the connection and entered the password I got from the previous step.
   - Used 'ls' to see files -> File name was '-', therefore I used cat ./- to access the file.
   - How to deal with dashes in file name: https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal

Level 2 -> 3
   - I opened the connection and entered the password I got from the previous step.
   - Used 'ls' to see files -> File name included spaces therefore I wrapped it in quotations to access the contents.
   - Dealing with spaces in file name: https://linuxhandbook.com/filename-spaces-linux/

Level 3 -> 4
   - I opened the connection and entered the password I got from the previous step.
   - I changed directory path with cd inhere/
   - I searched for all files with ls -a, ls alone didn't find the hidden file.
   - I accessed the file by using cat ./...filename


# Can't Fish
- First, I pinged Cloudflare's DNS server (1.1.1.1) with network on resulting in a succesful network test to destination server.
- The ping shows destination IP, amount of data sent and the time taken. 
- Next, I disabled network from settings and pinged the same server again.
- Ping failed with error message: Network is unreachable.
![Screenshot 2024-09-05 at 15 12 06](https://github.com/user-attachments/assets/7843d5bc-6321-47cc-9815-02932aa6cf32)

# Port Scanning
- I started by updating available software with 'sudo apt-get update'
- Next, I installed nmap with command 'sudo apt install nmap -y', and checked the version with 'nmap --version'
- Instructions found here: https://phoenixnap.com/kb/how-to-install-use-nmap-scanning-linux
- I disconnected my network and tested it with a ping to Cloudflare DNS server
- I ran the command 'sudo nmap -A localhost'

![Screenshot 2024-09-06 at 14 56 09](https://github.com/user-attachments/assets/3d2dfe9a-11a2-4194-82d1-1d3f0b7b3cf3)

- DNS server could not be determined since the scan was initiated without network connection.
- Only port scanned is for localhost therefore no other TCP ports were scanned.
- TCP port for SSH is 22 with SSH version 9.2p1 running on Debian
- Port 631 is for connecting IPP = Internet Printing Protocol, i.e. for printers.
- End breaks down basic information of device and OS version.


# Daemon
- I started by updating software again (just in case), and ran 'sudo apt-get -y install apache2'
- After a minute or two the installation was succesful, and I ran 'sudo systemctl start apache2' to start daemon.
- I disabled network and started the port scan.
- Essentially the results were the same, but there was a new port added:
     - Port 80 fro Apache on Debian as an HTTP server

![Screenshot 2024-09-06 at 15 16 38](https://github.com/user-attachments/assets/d805239e-5b64-4367-97aa-941d32159110)






