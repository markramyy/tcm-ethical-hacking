# Exploitation
---
## Basics

---
### 1. Shells:

---

- #Shell is access to a machine 

- **Reverse Shell** : it means that a victim connects to us, it will be used 95% of the time.

- **Bind Shell** : we have our attack box and then our target, we actually open up a port on the machine then we connect to it. it is most likely are going to be on an external assessment.

---
### 2. Staged vs Non-Staged Payloads

---

- #Payload is what we're going to run as an exploit, we use different type of payloads depending on what it is (Windows type payload - Linux type payload - meterpreter type payload - python - etc...).

---

|               **Non-staged**               |           **Staged**            |
|:------------------------------------------:|:-------------------------------:|
|     1.Sends exploit shellcode all once     |     Sends payload in stages     |
|   2.Larger in size and won't always work   |       Can be less stable        |
| 3. **EX**: windows/meterpreter_reverse_tcp | windows/meterpreter/reverse_tcp |

---
### 3. Brute Force 

---

- #Hydra is a brute force tool --> **hydra -l {user} -P  /usr/share/wordlists/metasploit/unix_passwords.txt ssh:// {IP:22} -t 4 -V**

- #metasploit --> auxiliary/scanner/ssh/ssh_login.

---
### 4. Credential Stuffing and Password Spraying

---

- It's just injection breach account credentials in hopes of account takeover.