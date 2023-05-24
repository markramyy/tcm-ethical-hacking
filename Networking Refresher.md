# Networking Refresher
---

## 1. IP Addresses

---

- **inet** #IPv4 is in decimal notation, it contains our IP address this is how we communicate over layer 3. (These Layers all refer to something called #OSI Model). If we're using IPv4 but we're out of address space? 

- We are using something called **NAT** which is network address translation, what we're doing is we're assigned these privates IP address spaces .

---

- If you ever seen a IP address before and you have been on a network good chances are, it probably started with 192 or maybe with a 10 dots. And that's because those are private IP addresses so anything that starts with 192.168 is not an IP address that is going to be out in the **interwebs**. 

- So because we can use these private IP addresses, we can pass them through what is called a public IP address.

- **inet6** #IPv6 is in hexadecimal notation
---

![[IP-Addresses.png | 600 ]]

---

## 2. MAC Addresses

- We are going to move to talk about layer 2 **(PS : IP is layer 3)**, here we're going to talk about a MAC address or a physical address.

- MAC stands for Media Access Control, that is identified here in our ifconfig as **ether**.

- It a way that we communicate when we are using #switches.

- MAC addresses have identifiers, it has 6 pairs of two. So the first 3 pairs here are identifiers,  and we can identify what we are up against.

---

## 3. TCP, UDP, and the Three-Way Handshake

---

- Now we're moving into layer 4, which is the transport layer of the #OSI model 

- Use a tool called **Wireshark** to capture data.

---

|                    **TCP**                    |         **UDP**         |
|:---------------------------------------------:|:-----------------------:|
|         Transmission Control Protocol         | User Datagram Protocol  |
| Think of it as a Connection Oriented Protocol | Connectionless Protocol |
|               HIGH Reliability                |   Streaming Services    |
|    Used in website (HTTP, HTTPS, SSH, FTP)    |   DNS or voiceover IP   |


- Check https://github.com/markramyy/ethical-hacking for more.

---

## 4. Common Ports and Protocols

---

### #TCP

- FTP (File Transfer Protocol) **{21}**  ==> we can log into the server, we can put a file or get a file off the server.

- Telnet **{23}**  ==> is the ability to log into a machine remotely in clear text. 

- SSH **{22}**  ==> Same as Telnet but it is the encrypted version of it.

---

- SMTP () **{25}** ==> Related to mail.

- POP3 () **{110}** ==> Related to mail.

- IMAP (Incoming Mail) **{143}** ==> Related to mail.

- DNS (Domain Name System) **{53}** ==> A way to resolve IP Addresses to names.

- HTTP **{80}**  /  HTTPS **{443}** ==> they are used for Websites. 

- SMB (Server Message Block) **{139 + 445}** ==> They are related to file shares, also called samba.

---

### #UDP

- DNS (Domain Name System) **{53}**

- DHCP (Dynamic Host Configuration Protocol) **{67 , 68}**  ==> associates you with an IP Address at random

- TFTP (Trivial File Transfer Protocol) **{69}** ==> It is the trivial FTP 

- SNMP (Simple Network Management Protocol) **{161}** ==> Information gathering specially if there are strings being used that are community or public strings.

---

## OSI Model

---

| **Layer Num** | **Used For** |       **Examples**        |
|:-------------:|:------------:|:-------------------------:|
|       1       |   Physical   |    Data cables , cat6     |
|       2       |     Data     | Switching , MAC Addresses |
|       3       |   Network    |  IP Addresses , Routing   |
|       4       |  Transport   |         TCP , UDP         |
|       5       |   Session    |    Session Management     |
|       6       | Presentation |     WMV , JPEG , MOV      |
|       7       | Application  |        HTTP , SMTP        |
|               |              |                           |

Note : Please Do Not Through Sausage Pizza Away

---

- When we receive data, it goes down from the physical layer all the way down to application **(1==>7)**.

- When we transmit data, it goes out the application layer up to physical **(7==>1)**.

- When we are troubleshooting, it is always best to start with the physical going down to application **(1==>7)**.
 ---

## Subnetting

---

- netmask in ifconfig ==> subnet mask(255.255.255.0).

- Subnet Guide : https://drive.google.com/file/d/1ETKH31-E7G-7ntEOlWGZcDZWuukmeHFe/view.

- Seven Second Subnetting : https://www.youtube.com/watch?v=ZxAwQB8TZsM

- You can use online subnetting : https://www.ipaddressguide.com/cidr

---
- Some Examples :

|   **IP/CIDR**   |   **Subnet**    | **Hosts** | **Network**  | **Broadcast** |
|:---------------:|:---------------:|:---------:|:------------:|:-------------:|
| 192.168.1.0/24  |  255.255.255.0  |    254    | 192.168.1.0  | 192.168.1.255 |
| 192.168.1.0/28  | 255.255.255.240 |    14     | 192.168.1.0  | 192.168.1.15  |
| 192.168.1.16/28 | 255.255.25.240  |    14     | 192.168.1.16 | 192.168.1.31  |
| 192.168.0.0/23  |  255.255.254.0  |    510    | 192.168.0.0  | 192.168.1.255 |
| 1992.168.2.0/23 |  255.255.254.0  |    510    | 192.168.2.0  | 192.168.3.255 |
|                 |                 |           |              |               |
| 192.168.0.0/22  |  255.255.252.0  |   1022    | 192.168.0.0  | 192.168.3.255 |
| 192.168.1.0/26  | 255.255.255.192 |    62     | 192.168.1.0  | 192.168.1.63  |
| 192.168.1.0/27  | 255.255.255.224 |    30     | 192.168.1.0  | 192.168.1.31  |

---