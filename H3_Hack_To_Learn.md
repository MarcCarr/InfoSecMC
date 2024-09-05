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



