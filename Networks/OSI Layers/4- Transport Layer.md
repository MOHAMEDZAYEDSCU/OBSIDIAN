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

>[!bug]- TCP Protocol:
>- most used, used for insurance of data transmission by flags.
>
>>[!caution]- Flags type:
>>- syn
>>- Ack
>>- fin
>>- push
>>- reset
>
>- validate reliable connection.
>- detect loss or failed in data.
>- filter duplicated data.
>- used for accurate not speed.
>
>>[!tip]- Three way handshake:
>>- you send (syn).
>>- it reply with (syn/Ack)
>>- you send (Ack).
>>- now you have your connection ;)

>[!bug]- UDP Protocol:
>- no handshake
>- no failure detection
>- no fkn fighting.... !!!
>- **Used when the speed more important than accuracy, audio or video.**

