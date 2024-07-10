
>[!todo]- What is it ?
>- an automatic tool that allow you to exploit vulnerabilities.
>- it has scripts that allow you to lunch it automatically
>---
>- it has a large database for vulnerabilities exploits

>[!caution]- Exploit :
>- استغلال
>- it is a code that allow you to access the victim machine
>- it depend on the vulnerability.
>---
>- Gaining access is a big reward.
>---
>- watch the metasploit video again, Bonus video in the first part for more info and how to use.


>[!caution]- How & When to use :
>- identifying a vulnerable service
>- searching for a proper exploit 
>- use scripts to exploit
>- inject payloads after gaining access
>---
>- you can use it after discover the vulnerability, so you want to exploit it.
>---
>- it has multiple commands like :
>	- search
>	- find
>	- exploit,
>	- show
>---
>>[!todo]- Steps :
>>- first of all before exploit.
>>- you should configure the metasploit app by :
>>	- enter the destination ip address
>>	- enter to targeted port
>>	- choose the scenario script for the exploitation.
>>		- each exploit take a specifc needs.
>>		- type `show payloads` for showing them for each vulnerability.
>>	- it would be useful in the beginning


>[!todo]- Steps :
>- using nmap for scan the target after the recon step
>- now you found open ports, so use nessus ..
>	- to tell you the vulnerabilities associated with each port ==(service)==
>	- now you have the names of the vulnerabilities,
>- go to metasploit and use it to exploit those vulnerabilities by its ready scripts.
>	- for gaining access in the target machine.

---

>[!caution] CVE :
>- common vulnerability exposure.
>- it links the vulnerability with a number and its discovery year.

---
>[!quote]- Thoughts Section :
>- you try an exploit script, if it failed
>- try another one ??
>	- for exp :
>	- Ftp has 20 types of exploits, so if one failed , just try another.
>- each payload has a specific characteristics
>	- one for os shell
>	- another for meterpreter shell
>		- very dangerous
>		- used for controlling the target machine
>		- open camera, microphone or downloading files ..
>- you can make your own payload and send it.
>- need to understand the ascii code, reverse engineering and of course the programming language used.
>	- you should watch people do that to understand the concept and how to design your malware to perform a specific task.

