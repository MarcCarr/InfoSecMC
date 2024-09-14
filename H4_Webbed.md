# OWASP: OWASP 10 2021

## Broken Access Control
- Attacker gains priviledged / admin control of a site by manipulating the site's framework to bypass access control checks. E.g:
    - URL modification
    - API access with vulnerabilities
    - Cookie tampering

- Access control must be managed in server-less API or trusted server-side code to prevent attackers from having a chanche at manipulating the control check logic or metadata.


## Security Misconfiguration
- Application security is configured with redundancies, inconsistancies, available detailed error handling logs, or overall negligence.
- Misconfiguration can be prevented with a minimal platfrom created in harmony that implements clear boundries, varying credentials, and automated capabilities.


## Vulnerable and Outdated Components
- Lack of awareness to used components and versions in full framework can lead to unknown security holes.
- Software must be up to date and supported to mitigate vulnerabilities.
- Regular system checks must be conducted, and underlying issues can't be left to fester.

## Injection
- User is able to gain access to sensitive data by injecting their own command using framework language like SQL or OS command.
- Injection can be mitigated by implementing the same structure for the entire database. Injections capabilites lessen when built-in security is consistant.
- Using a safe API to avoid using the interpreter.


# F12
- The installation process for Webgoat failed the first time after installing Java and a firewall which took just over an hour. 
- I used the newest version (v2023.8) of Webgoat found here: https://github.com/WebGoat/WebGoat/releases
- Installation of the Github jar worked, but changing the deafult port did not work – the change was very slow, and after about 45min the VM crashed.
    - Re-opening the VM straight after also didn’t work properly
    - The VM booted into the CLI rather than GUI.  I used ’sudo systemct1 start gdm’ to start GUI.
    - Once GUI started up, I wasn’t able to log in. VM accepted the password, but the log in took about 10min, and returened to log in screen.

- The next day, I repeated the installation, and default port change for Webgoat, and both worked. Took about 35min.
- I opened Firefox browser to http://127.0.0.1:8888/WebGoat, which took another 20min.
- I tried registering, but the page loaded for about 15min, and the VM gave me an error message that Firefox was not responding.
- I tried to click ’Wait’ a few times, and ’Force quit’, but the VM was not responding, and eventually crashed.
- I didin't have time to try again.


# SQLZoo
- 0 SELECT basics
    - Three subtasks required small modifications to ready made SQL code.
    - 1st, I replaced 'France' with 'Germany'
    - 2nd, I replaced 'Brazil', 'Russia', 'India' and 'China' with 'Norway', 'Sweden', 'Denmark'.
    - 3rd, I replaced 250,000 and 300,000 with 200,000 and 250,000
 
- 2 SELECT from world.
    - 1st didn't reuqire any changes as it was illustrating the results when looking at the full table.
    - 2nd, I changed WHERE population = 64105700 -> WHERE population > 200000000
 

 # Johnny tables
I started by opening the example web page and browsing around the different products and categories. I looked for a field where I could insert text, but there wasn't one so I looked the URL more carefully. When looking at a specific category, the URL ended with e.g. "category=Accessories". Comparing this to the example query provided in the task instructions, I thought I could modify the URL to exploit the vulnerabilty here.

- I wasn't sure where to begin or what to add to the URL so I read through this: https://portswigger.net/web-security/sql-injection#how-to-detect-sql-injection-vulnerabilities
- The "Retrieving Hidden Data" section had the answer ready, which I added to the site's URL. I took away the 'category' part and added: 'OR+1=1--.
    - Taking out the category and replacing it with a singel quotation mark results in an empty category field
    - OR+1=1 gives the query a conditional that always evaluates to true
    - "--" is SQL syntax for a comment, which negates the rest of the query that has the check for 'released'.
- The website now shows all items. 
 
