>[!faq]- What is it?
>- the second layer of OSI model.
>- responsible for node to node delivery data and Make the devices communicate through the same network using MAC address.
>- Network Switches and access points operate in this layer.
>- the data and the mac address in this layer called frames and in the **network layer called packet**.
>- the most complex layer because it hides the complexity of physical layer from above layers.

## ARP Protocol:
>[!tip]- About: 
>- The Address Resolution Protocol (ARP) is used to map IP addresses to their corresponding MAC (Media Access Control) addresses within a local network.
>- he send a request, Who has this IP (destination IP)? with the broadcast message(ff:ff:ff:ff:ff:ff) and the targeted device will answer with his mac address.
>- Both devices temporarily store each other's IP and MAC addresses in their ARP cache for future use.
>---
>>[!caution]- broadcast IP:
>>- The ARP request is sent to the broadcast MAC address (ff:ff:ff:ff:ff:ff), which ensures that all devices on the local network receive the request.
>---
>>[!caution]
>>- You can use the `arp` command in the terminal to view the ARP table, which lists the IP and MAC addresses that have been recently resolved.
>>- use request & reply
>---
>>[!bug] - ARP is able to be spoofed. An attacker can send falsified ARP messages to associate their MAC address with the IP address of another device. This allows the attacker to intercept, modify, or stop data intended for the target device.
>---- 
>>[!tip]- **Key Points:**
>>- ARP uses request and reply messages.
>>- ARP cache stores mappings temporarily for efficiency.
>>- Vulnerable to ARP spoofing attacks.
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

