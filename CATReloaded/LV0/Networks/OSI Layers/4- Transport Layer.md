>[!faq]- What is it?
>- ensure reliable data transfer between hosts.
>- determine the success of data transmission and if there are any problems, it tell your device to send the data again.
>- there are TCP, UDP.
>- reorder packets to retrieve the data by sequential identifier.
>- first chose the port to identify the service used then the protocol, {TCP or UDP}.

>[!tip]- Port:
>- **is for identifying unique services on the same host**.
>- there are 65.500 port on TCP Protocol and UDP either.
>
>>[!caution] 1 to 1023:
>>- well known ports (http, https, ftp, ssh, dns).
>
>>[!caution] 1024 to 49100.
>>- available for your usage.
>
>>[!caution] The remaining:
>>- operating system use those ports in outgoing connection.
>
>>[!example]
>>- HTTPS port 443, secured web traffic.
>>- port 80 for web traffic.
>>- port 25 (SMTP) for mails, and so on
>>- it is like provide multiple channels for different services !!

## Types:

>[!todo]- TCP Protocol:
>- most used, used for insurance of data transmission by flags.
>---
>>[!caution]- Flags type:
>>- Syn 
>>	- to start the connection, like `as-salam alikum`...
>>- Ack 
>>	- to ensure that the data is sent successfully of the connection is established
>>	- if connection successful, the `Ack` will be large that `Seq` by 1;
>>	- `seq` 
>>		- is a number you send with `Syn` flag.
>>- Fin 
>>	- finish the connection from both sides
>>- push 
>>	- i will send a data to a packet
>>- RST 
>>	- reset for terminate the connection from one side immediately
>>- URG 
>>	- urgent data and need to be processed directly
>---
>- validate reliable connection.
>- detect loss or failed in data.
>- filter duplicated data.
>- used for accurate not speed.
>---
>>[!tip]- Three way handshake: {tcp connect / full open scan.}
>>- ![[Pasted image 20240703143617.png]]
>>---
>>---
>>- you send (syn). with the port to know open ports.
>>- it reply with (syn/Ack), so the port is open
>>- you send (Ack).
>>- now you have your connection ;)
>>	- if you send reset after the ack, the connection will be terminate, you just want to know if the port is open or not.
>>- if it reply with RST instead of syn/Ack, so the port is closed.

>[!bug]- UDP Protocol:
>- no handshake
>- no failure detection
>- no fkn fighting.... !!!
>- **Used when the speed more important than accuracy, audio or video.**

