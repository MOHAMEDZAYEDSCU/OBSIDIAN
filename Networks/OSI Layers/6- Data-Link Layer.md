>[!faq]- What is it?
>- the second layer of OSI model.
>- responsible for node to node delivery data and Make the devices communicate through the same network using MAC address.
>- Network Switches and access points operate in this layer.
>- the data and the mac address in this layer called frames and in the **network layer called packet**.
>- the most complex layer because it hides the complexity of physical layer from above layers.

## ARP Protocol:
>[!tip]- About: 
>- Address Resolution Protocol (ARP)
>- He ask with the IP to know the mac address by sending (ff:ff:ff:ff:ff:ff) with the broadcast ip to make all devices pay attention.
>- he send a request, Who has this IP (destination IP)? and the targeted device will answer with his mac address.
>- both devices store the IPs and MAC addresses for each other temporary in ARP cache for future use.
>---
>>[!caution]- broadcast ip:
>>- is the ip which all devices pay attention to with the ff:ff:ff:ff:ff:ff to discover all devices on the network or sending messages to them.
>---
>>[!caution]
>>- you can use command arp in the terminal to show all internet and mac addresses.
>>- use request & reply
>---
>>[!bug] - easy to be spoofed, the hacker device can tell the questioner that he has the ip address he asked for and let him store his mac address and hacker device take all the data. 
## Sub-layers of the Data Link Layer:
>[!quote]- Logical link control (LLC):
>- deal with multiplexing تعدد الارسال
>- deal with the flow of data between application
>- providing error message and aknowledgments.
>- ensurance of data transmission by checking frames.

>[!quote]- Media Access Control (MAC):
>- responsible for addressing frames and controls physical media access.
>- consists of 6 parts (00:11:22:33:44:55)
>- first 3 parts is for the manufacturer and the other for the device id.
>- can be spoofed -> يتم سرقته او انتحال شخصيته
>
>>[!important] **Switch** deal with it to determine which device you will send the data to.

