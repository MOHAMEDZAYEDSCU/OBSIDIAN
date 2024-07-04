
 >[!todo]  [[2_Scanning|ZEN Map]]
 >- try to download it if possible
 >- the graphical interface will make it beautiful.
 
---

 >[!caution]- About
 >- it is a tool that collect data about dns and its ports.
 >- ==it is work on TCP ports by default, if you want a UDP scan you will use different parameter ..!!!==
 >- it has a lot of scripts to test all ports and dns and bypass security features like firewall also!!!
 >- ==it is a part of scanning not info gathering==
 >- a very important tool and will be used a lot forward ...
>---
>- download the nmap sheet cheat ..

---
---

>[!bug]- Using NMAP as a decoy!!
>- ![[Pasted image 20240703222720.png]]

---
***
#### How to use :

- always use man in the beginning for more information and arguments. 
---
---
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
	 - like version of the service
---
- `nmap [IP] -p portNo`
	- for scan a specific port in an IP.
	- `-p 1-100`
		- to test ports 1 to 100 only.
---
- `nmap -sS -F [IP]`
	- you use `-F` to split the packets to bypass the firewall...
---
- `nmap [IP] -p-`
	- scan for all the possible ports (65535)
---
- ==For the UDP ports :==
	- `nmap [IP] -p- -sU`
		- for scan all UDP ports
		- will take alot of time
	- `nmap [IP] -p 1-200 -sU`
		- will scan for the first 200 port that work as UDP.
---
***

>[!Caution]- Cheat sheet :
>- ![[Pasted image 20240704124515.png]]
>---
>***
>- ![[Pasted image 20240704124608.png]]

---
---

