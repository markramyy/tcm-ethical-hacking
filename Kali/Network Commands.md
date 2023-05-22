# Network Commands

---

|                             **OLD School**                              |                                    **New School**                                    |
|:-----------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
|                                ifconfig                                 |                                         ip a                                         |
|                               plain text                                |                                  nice and colorful                                   |
| in some instances requires sudo to run or may no longer be on a machine | is not a machine depending on what type of machine you're on and what is your access |
|                         only shows the Ethernet connections , hardwired connections                         | does all                                                                                     |

---

- If we want to see wireless connections, we need to do **iwconfig** 

- **ip n** : stands for ip neighbor and has an alternative **arp -a** (Address Resolution Protocol ).
	- Now arp says "what IP address is associated with what MAC address ? " , what happen is a broadcast message goes out when we are trying to identify and IP and MAC address.

---

- **ip r** : stands for ip route and you can also type route and you will get similar feedback.
	- Now we are looking at is called a routing table. we want to know where our traffic is routing. 
	- In real life pentest,  we have been on a quote unquote segmented network and in reality it, it really wasn't a segmented network (no route to that network), so you are isolated and can't access to anything.

---

- **ping** : with this command you're checking if the ip is there(available)  and it uses something called **ICMP** traffic.

- **netstat** : is used to identify what open ports and services are there.
