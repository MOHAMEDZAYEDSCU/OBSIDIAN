>[!FAQ]- What is it?
>- connecting separate network together to allow devices to connect.
>- router (default gateway) operate at this layer.
>- it is like make a bigger network from small networks.
>- devices communicate with **IP address**

## How it work?
>[!tip] Concept:
>- It's like querying about the IP address till is found, switches then routers.
>- you can use ipconfig in linux to show your ip.

>[!caution] Default gateway:
>- is the IP of router.
## Types?

>[!example]- IPv4:
>- Internet Protocol.
>- currently used
>- consists of 4 parts separated by a dot, each is 8 bit (numerical).
>- each one part determining the network, see the classifications.
>- form 0 to 255.
>- the number of network and IP depend on those numbers.
>- classified into 5 Classes:
>
>>[!quote]- A:
>>- first 8 bit determining the network.
>>- small number of network and large number of IP.
>>- from 0 to 127 -> 0.0.0.0 to 127.0.0.0
>
>>[!tip]- B:
>>- first 16 bit determining the network.
>>- equal number of switches network and IP.
>>- from 128 to 191 -> 128.0.0.0 to 191.255.0.0
>
>>[!success]- C: (important)
>>- first 24 bit determining the network.
>>- large number of network and small number of IP
>>- from 192 to 223 -> 192.0.0.0 to 223.255.255.0
>
>>[!quote]- D:
>>- all bits.
>>- used for multicast
>>- 224 to 239 -> 224.0.0.0 to 239.255.255.255
>
>>[!quote]- E:
>>- all bits
>>- used for reserved for experimental.
>>- 240 to 255 -> 240.0.0.0 to 255.255.255.255

>[!example]- IPv6:
>- in the future
>- 128 bits - 8 sections
>- in hexadecimal 


## Reserved Addresses:
- reserved IP addresses are those that are set aside for specific purposes and should not be assigned to devices on a network.

>[!caution]- **Loopback Address (127.0.0.1)**:
>- used for communication within the device itself.

>[!danger]- **Private IP Addresses**:
>- These addresses are reserved for use within private networks and should not be routed on the public internet.
>
>>[!example]- Examples:
>>- **Class A**: 10.0.0.0 to 10.255.255.255 (10.0.0.0/8)
>>- **Class B**: 172.16.0.0 to 172.31.255.255 (172.16.0.0/12)
>>- **Class C**: 192.168.0.0 to 192.168.255.255 (192.168.0.0/16)

>[!caution]- Local Addresses:
>- Automatically assigned when no other IP address configuration is available.

## More Important info:
#### Sub-net Mask:
>[!caution]- What is it?
>- identify the network and the host.
>- like the first 16 bit for the network and other for IP, IPv4-B
>- mentioned before in IPv4.
#### CIDR
>[!caution]- What is it?
>- classless inter domain routing.
>- another simple way to represent network and devices section, to know what type of network it is, like (A, B, C, ...).
>- in A, you can use 10.0.0.0/8 -> for 8 bit network (N).
>- in B, you can use 172.16.0.0/16 -> for 16 bit network (N).
#### DHCP:
>[!caution]- What is it and How it work?
>- dynamic host configuration protocol.
>- DHCP discovery. to tell the router he need an IP and access to the network.
>- DHCP Offer:  by the router to give you an IP.
>- DHCP request:  to accept the IP given
>- DHCP Ack:  To Confirm that he give you that IP.
#### Routing:
>[!caution]- What is it?
>- The Path which packets moves between networks.
>- **Router**: have multiple interfaces and can access multiple networks at the same time.
#### TTL:
>[!caution]- What is it?
>- time to live
>- fixed number, almost 64 or 128 (maybe varies ?!!)
>- the number of networks you surpass before the packet lost
>- found to destroy infinite loop while packet travel.
#### Routing Table:
>[!caution]- What is it?
>- it is determining the destination node and the network path, if there are multiple paths, it will chose the shortest one.

>[!caution]- Routing Protocol:
>- for determining :
>	- next hop
>	- shortest path
>	- network changes
>	- link failure
>
>>[!bug] Types:
>>- RIP: determine the shortest path and broadcast routing table every 30 second
>>- OSPF: detect changes in network topologies and link failure.
>>- BGP : most used, determine the shortest path and if route fail it change to another one.

>[!caution]- NAT Protocol:
>- network address translation.
>- all LAN Protocol using NAT.
>- there are private and public IP
>- ![[Pasted image 20240411210306.png]]
>- a lot of private IP and they has the same public IP as the router.

>[!caution]- ICMP Protocol:
>- test connectivity between nodes.
>- using ping instruction in linux.
>- ICMP echo request sent from the sender device to the destination device with his ip and the destination ip and the destination device send ICMP reply to him.

>[!tip]- How trace route work?
>- first the device make TTL(time to live) with 1 and it goes to the first router then decrement to 0 without reaching the destination address so a request fail will occur, then let it 2 and repeat until the destination device send ICMP reply and by that you determine the TTL.

