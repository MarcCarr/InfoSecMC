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


# SQLZoo
- 0 SELECT basics
    - Three subtasks required small modifications to ready made SQL code.
    - 1st, I replaced 'France' with 'Germany'
    - 2nd, I replaced 'Brazil', 'Russia', 'India' and 'China' with 'Norway', 'Sweden', 'Denmark'.
    - 3rd, I replaced 250,000 and 300,000 with 200,000 and 250,000
 
- 2 SELECT from world.
    - 1st didn't reuqire any changes as it was illustrating the results when looking at the full table.
    - 2nd, I changed WHERE population = 64105700 -> WHERE population > 200000000
 

 
 
