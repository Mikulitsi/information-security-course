# h4 Johnny Tables

## OWASP: OWASP 10 2021

### A01:2021 - Broken Access Control
 - A failure to enforce access control policies, which can allow unauthorized access, modification, or privilege escalation. 
 - Common issues include:
   - least privilege violations
   - missing API method controls
   - CORS misconfigurations
 - To prevent these issues:
   - deny by default (least privilege)
   - rate limiting APIs
   - removing sensitive files from web roots
   - logging access control failures
   - notifying administrators when necessary.

### A05:2021 - Security Misconfiguration
- App or environment is not safely configured, and may have weak configurations or default passwords still in use.
- Common issues include:
  - Leaving sample apps or default accounts active in a live environment.
  - Running old or outdated versions and not applying security patches..
- To prevent these issues:
  - Have a secure setup process that is consistent across all environments.
  - Remove anything unnecessary.
  - Update and review configuration and permissions regularly.
  - Apply security checks and use security headers automatically.
- It is really important to prevent these issues as hackers can easily find and exploit weaknesses to steal data or take control of systems.
    

### A06:2021 - Vulnerable and Outdated Components
- Common issues include:
  - Use of components that have a publicly known exploit and are not currently patched.
  - Dependencies that are no longer actively maintained or updated by their authors.
  - Inclusion of third-party components without awareness of their security status.
  - Components that expose sensitive data or functionality due to vulnerability.
- To prevent these issues:
  - Regularly update and patch components to the latest version.
  - Use tools to check for known vulnerabilities.
  - Test components in a pre-production controlled environment.

### A03:2021 - Injection
- Common issues include:
  - SQL Injection: Malicious SQL queries inserted into input fields.
  - Command Injection: Untrusted user input can be utilized to execute any arbitrary commands on the target system
  - NoSQL Injection: Attacks targeting NoSQL databases.
  - LDAP Injection: Input fields can be manipulated to allow attackers to write LDAP queries, which result in arbitrary commands being executed to the underlying operating system.
  - OS Injection: Malicious injection of operating system commands.
- To prevent these issues:
  - Practice least privilege for any access to database or system..
  - Conduct security testing specific emphasis on injection vulnerabilities.

## Munroe
- The comic focuses on SQL injection. Malicious code can be executed when user input is not properly sanitized.. 
- Emphazises the means to clean and validate any data entered by a user before incorporating whatever the user input into a database query.  

## a) Goat. Install WebGoat 2023.4
<img width="786" height="392" alt="image" src="https://github.com/user-attachments/assets/951f23a3-b549-4c9f-bf7e-3f015a3b1dc4" />

- I had already done this task but didn't get screenshots so that's why it shows that nothing was upgraded or installed in the screenshots.

<img width="1907" height="736" alt="image" src="https://github.com/user-attachments/assets/7512f465-8c25-4609-ba14-114b2cd1d4ba" />

<img width="808" height="63" alt="image" src="https://github.com/user-attachments/assets/9384c583-4bff-4fa0-bb7f-967fe81e4871" />

- In the end of installing Webgoat and running it, it gives the link to browse Webgoat.

## b) Webgoat 2023.4: General: Developer Tools
- First task required to open the console and add input webgoat.customjs.phoneHome(). Adding the input gave a phone number that had to be copied and pasted.

<img width="1919" height="922" alt="Screenshot 2025-09-16 045915" src="https://github.com/user-attachments/assets/1243e584-a4b5-4147-905e-bf01e1e8d565" />

- After clicking the request button, I go the inspect mode and go to network. I find the network file there, click that and then click the request tab. Inside that request tab was the number needed to complete the task.

## c) Update all operating system and all applications in your Linux
<img width="1411" height="772" alt="image" src="https://github.com/user-attachments/assets/13653715-402f-491a-bdc7-4bd3ac9ff5e5" />

- I needed commands:
  - sudo apt update
  - sudo apt-get upgrade
  - sudo apt-get dist-upgrade
 
- I had done this earlier already so that's why it shows that nothing was updated in the screenshots.

## d) SQLZoo
<img width="1257" height="877" alt="image" src="https://github.com/user-attachments/assets/c571858d-d61f-4174-a43f-812a02fbfb24" />

<img width="982" height="521" alt="image" src="https://github.com/user-attachments/assets/d235e16f-f18c-44a2-bdce-b1dbf4cf4046" />

<img width="996" height="501" alt="image" src="https://github.com/user-attachments/assets/718fa294-1437-4114-86d9-3e2fb2168ac0" />

<img width="1252" height="850" alt="image" src="https://github.com/user-attachments/assets/2dbc294c-4562-46ac-85cd-b3b5291bb7a0" />

For me these tasks were really simple as I'm having a data management and databases course at the same time as this InfoSec course so I have knowledge of the some really basics SQL inputs.

## e) Portswigger Labs
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6144fbc7-f16d-438a-956b-0cc3692f54de" />

# Sources
- https://owasp.org/Top10/A01_2021-Broken_Access_Control/
- https://owasp.org/Top10/A05_2021-Security_Misconfiguration/
- https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/
- https://owasp.org/Top10/A03_2021-Injection/
- https://xkcd.com/327/
- https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/
- https://www.manageengine.com/patch-management/debian-updates.html
- https://sqlzoo.net/wiki/SQL_Tutorial
- https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data
- https://www.youtube.com/watch?v=X1X1UdaC_90
