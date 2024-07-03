
 >[!todo]  [[2_Scanning|ZEN Map]]
 >- try to download it if possible
 >- the graphical interface will make it beautiful.
 
---

 >[!caution]- About
 >- it is a tool that collect data about dns and its ports.
 >- it has a lot of scripts to test all ports and dns and bypass security features like firewall also!!!
 >- ==it is a part of scanning not info gathering==
 >- a very important tool and will be used a lot forward ...

---
---
#### How to use :

- `nmap [ip]`
	- normal scanning for open p
---
- `nmap -sV [ip]` 	
	- give you more info like
		- version and the host system type, ubuntu, kali, ...
---
- `nmap -O [ip]`
	- give you more info about the operating system of the ip.
---
- `nmap -sn [ip/net-mask]` :
	- to scan for hosts in the network.
	- you should provide the category, A, B,C, D or E with the number of bits.
		 - A -> 8
		 - B -> 16 
		 - and so on....
---
 - `nmap [ip]` :
	 - it will search for open ports in the first 1000, the most known.
---
 - `nmap -sV [ip]`:
	 - searching for open services(ports) with a lot of detail..

---
---
