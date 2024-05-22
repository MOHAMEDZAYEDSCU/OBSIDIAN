>[!caution]- What is it?
>- The steps a penetration tester takes during an engagement is known as the methodology.
>	 A practical methodology is a smart one
>
>>[!important] Careful:
>>- methodology that you would use to test the security of a web application is not practical when you have to test the security of a network.

>[!important]- Stages of it?
>- info gathering:
>	- This stage involves collecting as much publically accessible information about a target/organisation as possible, for example, OSINT and research.
>		- **Note:** This does not involve scanning any systems.
>---
>- Enumeration/Scanning:
>	- This stage involves discovering applications and services running on the systems.
>		- For example, finding a web server that may be potentially vulnerable.
>---
>- Exploitation:
>	- This stage involves leveraging vulnerabilities discovered on a system or application.
>	- This stage can involve the use of public exploits or exploiting application logic.
>---
>- Privilege Escalation:
>	- The attempt to expand your access to a system
>	- You can escalate horizontally and vertically:
>		- horizontally:
>			- is accessing another account of the same permission group (i.e. another user)
>		- vertically:
>			- that of another permission group (i.e. an administrator).
>---
>- Post-exploitation:
>	- **1.** What other hosts can be targeted (pivoting)
>	- **2.** What additional information can we gather from the host now that we are a privileged user
>	- **3.**  Covering your tracks
>	- **4.** Reporting
>

>[!success]- OWASP(open web application security project)
>- write reports stating to the top 10 vulnerabilities for web applications

