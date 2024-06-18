
## Network Exploration and Security:

>[!caution]- Net Cat:
>- tool for creating network connections, port scanning and file transfer
>---
>>[!quote]- Example of use:
>>- nc -v -z 192.168.50.5 1-100
>>	- nc => the main instruction.
>>	- -v  => provide more detailed output, which can be helpful for understanding the connection process.
>>	- -z => allows Netcat to report open ports without actually establishing a connection.
>>	- 192.168.50.5 => the ip of the target host.
>>	- 1-100 => specify the range of ports to scan, from 1 to 100.

>[!tip]- ifconfig:
>- **for changing IP address, broadcast or even MAC address as you want for security purposes.**
>---
>>[!caution]- Instruction Examples:
>>- ifconfig eth0 (up,down) :
>>	- for activating/disabling the network, wifi ?!
>>---- 
>>- ifconfig:
>>	- showing network interface.
>>----
>>- ifconfig eth0 {ip}:
>>	- changing current ip with the new one you entered.
>>----
>>- sudo ifconfig eth0 hw ether {the mac address you want} :
>>	- for changing the network mac address (router)? with the one you type.
>
>>[!bug]- Example of use:
>>- **sudo ifconfig eth0 192.168.1.100 netmask 255.255.255.0**
>>	- ==for manually assign IP to the current network interface as 192.168.1.100 and the netmask value is for specifying the network and host bits==.
>>	.--------------------------------------------------------.
>>	- sudo ifconfig:
>>		- known before.
>>	- eth0:
>>		- network interface typically named eth with a number 0 for the first interface.
>>	- 192.168.1.100:
>>		- your interface network (private ip)?.
>>	- netmast:
>>		- the instruction for requesting a new private ip.
>>
>>- 255.255.255.0 or 192.168.1.0/24 => for representing the **ip bits** of the network and ip bits of hosts. see [[5- Network Layer#Sub-net Mask|Sub-net Mask]] & [[5- Network Layer#CIDR|CIDR]] & [[5- Network Layer#DHCP|DHCP]].
>
>>[!caution]- Advantages:
>>- solving some network problem.
>>---
>>- more security for variety purposes.
>>---
[](5-%20Network%20Layer.md#Sub-net%20Mask)](5[](5-%20Network%20Layer.md#CIDR)d[][](5-%20Network%20Layer.md#DHCP)d receiver.
>>	- ==sudo ifconfig eth0 mtu 1500==
>>---
>>- modify the mac address of the the network interface (router)?.
>>	-  ==sudo ifconfig eth0 hw ether 00:11:22:33:44:55==
>>---
>>- enabling or disabling arp protocol.
>>	-  sudo ifconfig eth0 arp.

>[!tip]- netstat {}:
>- provides information about network interfaces, routing tables, and active network connections.
>
>>[!caution]- Arguments:
>>- -t => focus on tcp connection.
>>- -u => focus on udp connection.
>>- -s => statistics about network interface {ip, tcp or udp protocols}

>[!success]- nslookup {}:
>- name server lookup.
>- querying DNS (Domain Name System) servers to obtain domain name or IP address information.
>
>>[!caution]- Arguments:
>>- -type=ns {DNS}:
>>	- for known the base server or authoritative domain for the IP server.
>>- -type=mx {DNS}:
>>	- showing the mail exchanger domain of the IP address.

>[!success]- dig {}:
>- domain information groper.
>- for indicate all DNS information.
>
>>[!caution]- Arguments:
>>- see --help or man dig for the arguments.

>[!caution]- Ping Command:
>- Utility used to check whether a network is available and if a host is reachable. With this command, you can test if a server is up and running it
>- ping {any argument} hostname, ping -c 5 google.com

## System Administration:

>[!bug]- About system users:
>- w, who:
>	- displaying the system users.
>	- w for display the users with last time logged in.
>
>>[!caution] Swap between them:
>>- use:
>>	- su username => for normal admin
>>	- sudo su root => for root admin.
>
>>[!danger] Execution as Another admin:
>>- sudo -u username command => execute a command as another user. This is often used for administrative purposes.

>[!caution]- wall:
>- write all (w`rite` all).
>- for informing all the system user about something.
>- wall "what ever you want.".

>[!caution]- free:
>- information about ram and memory, total and used.

>[!caution]- ENV:
>- for showing environment variables and modify them.

>[!success]- uptime:
>- for monitoring system usage by time initiated and spended in it with the user number and load average.
>- for detecting if anyone use your system or access it and have any information from it.

>[!danger]- .bashrc
>- it is the file with all instruction you use in linux with its formatting
>- you can use export PATH in the terminal to make it for the current session only.
>
>>[!caution]- PATH:
>>- is the locations for all instructions in linux separated by `:` 
>>- **execute the instruction by its name.**
>>- for example:
>>	- you have a file in desktop and put an executable file in it.
>>	- then go to .bashrc file and put the direction of the folder desktop in the export PATH: by  ==export PATH=/home/desktop:$PATH== => to search for instructions in the desktop directory and save the file with the new update ==in the current user only==.

>[!danger]- Privilege Escalation:
>- تصعيد الامتيازات
>- try to gaining authority on the victim system, used for hackers.
>- there are horizontal and vertical.

>[!bug]- mkpasswd:
>- for generating a difficult password !!.

>[!tip]- &
>- run a command in the background?
>	- ./my_script.sh &


## File Encryption using gpg:

>[!danger] Careful:
>- save the password in location for not forgetting it.
>
 >>[!success] Encryption:
 >>- gpg -c --no-symkey-cache {filename}.
 >---
 >>[!caution] Decryption:
 >>- gpg --no-symkey-cache {filename}.
 >>	- for decryption.

>[!todo]- OpenSSH:
>- secure shell protocol in linux that allow you to access remote system.
>- there was an app do this connection !!!
>- support password based and key based authentications.

>[!success]- Logs
>- journalctl -n
>	- for displaying the last 10 login to the system.
## mapping:

#linux