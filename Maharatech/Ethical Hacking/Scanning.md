>[!caution]- About:
>- for discovering :
>	- live hosts and IPs.
>	- open ports and services.
>	- the operating system. (to detect your methodology)

---

>[!success]- TCP vs UDP:
>- ![[4- Transport Layer]]

---

>[!caution]- NMAP or ZEN MAP:
>- the difference between them is the graphical interface of zenmap.
>- it is like ping command:
>	- [[Advanced Kali LINUX| ping command]]  the last command in the list.
>	- for discovering open ports and its protocols.
>- with the graphical interface, you will find all the commands you need.
>---
>- There are Script that aid you to specify the method you will need to lunch your attack.
>--- 
>>[!tip]- How to use:
>>- nmap ip
>>	- normal scanning for open p
>>----
>>- nmap -sV ip 
>>	- give you more info like
>>		- version and the host system type, ubuntu, kali, ...
>>---
>>- nmap -O ip
>>	- give you more info about the operating system of the ip.

----

>[!success]- Banner Grabbing:
>- having the banner or basic information in the web servers versions and try to gain access
>---
>>[!tip]- Tools:
>>- telnet :
>>	- for remote access command line connection
>>	- but we use it to check specific services on specific ports.
>>	---
>>	- telnet Dns prot.no
>>	---
>>---
>>- netcat :
>>	- the same as previous
>>	---
>>	- nc -vv Dns port
>>		- -vv -> for more information.
>>	- you can use GET to know more information about your connection.

--- 

>[!danger]- Nessus:
>- for vulnerability scanning.
>- 





