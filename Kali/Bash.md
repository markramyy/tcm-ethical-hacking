# Scripting with  Bash

---

## 1. ping sweep

---

- Basically we're gonna go out and say, I wanna ping a device, if that device is alive, go ahead and show me that result and we're going to sweep an entire network.

- First, we're going to identify a device that's alive so we can test it out and then build upon that by using the command **ifconfig**.

- We can ping the IP by using packets and can control the number of packets transmitted and save it in a file. Command : **ping { IP Address } -c 1 > ip.txt**

---

## 2. grep

---

- grep is going to look for a specific term or phrase, and we can do that and it's gonna pull down any line that has that term or phrase.

- Command : **cat ip.txt | grep "64 bytes"** 

- If we're building out a ping sweeper what i wanna do is to sweep every single IP within a specific subnet. So when we run this on a bigger scale, we're going to need to grep out this information and extract it to where we only just get the IP address back.

---

- Command : **cat ip.txt | grep "64 bytes" | cut -d " " -f 4 | tr -d ":"**

	1. **cat ip.txt** : reads the contents of the file "ip.txt" and displays them.
	
	2. **grep "64 bytes"** : is used to search for specific patterns in text "64 bytes".
	
	3. **cut** : is a tool used to extract specific sections of text.
	
	4. **-d " "** : n this case, it uses the space character (`" "`) as the delimiter (`-d`).
---

5. **-f 4** : selects the fourth field (`-f 4`) from each line.

6. **tr -d ":"** : is used to delete characters. The `-d ":"` option specifies that the colon (":") character should be deleted from the output.

---

## 3. Bash

---


```Bash
#!/bin/bash 
if [ "$1" == "" ]
then echo "You forgot an IP address!" 
echo "Syntax: ./ipsweep.sh 192.168.1" 
else 
for ip in `seq 1 254`; do
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
done 
fi

```

---

- Now we have a list of IP addresses, let's say that we want to run [[nmap]], it's a tool that allow us to go out and do port scanning.

- Command:        **nmap -T4 -A -p-**        ||        **nmap {IP} 192.168.x.x**

- After we found the running IP addresses using the previous bash script. We'll make it pritn the IP addresses in a file. Command : **./ipsweep.sh 192.168.1 > ips.txt**

---

- Now you have a file contains all the running IP addresses. After that we're going to use #nmap to scan over these IP addresses

- Command: **for ip in $(cat ips.txt); do nmap $ip; done**

