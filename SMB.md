# Enumerating SMB

---
## SMB

---

1.  #SMB port 139/tcp

2. It's a file share, it commonly used in work environments and internal environments.

3. Tools to use for it : **nmap -->  metasploit framework --> smbclient**

---
### Tools

---
#### 1. Nmap

- Use it to find if the SMB (139/tcp) port is open and collect information from it.

---
#### 2. Metasploit framework

- Open it using **msfconsole** --> it is an exploitation Framework console (Recon - Exploit - Payload - Loot).
- Search for the selected port --> **msf5 > search smb**
- Find the auxiliary module and then search for the type of action that you want to do for our case now it's scanning --> **auxiliary/scanner/smb/smb_version**.
- Then you just use it --> **use auxiliary/scanner/smb/smb_version {the number}**.
- Then type **info** to see any information or **options**.
- Set the Target IP in the host section  --> **set RHOSTS {IP}** and then you type **run**.
- Make sure to document the output from the framework.

---
#### 3. smbclient

- smbclient is going to attempt to connect to the file share that's out there.
- Syntax --> **smbclient -L \\\\{IP}\\}**
- Then you choose the Sharename to dig in a little deep --> **smbclient \\\\{IP}\\{Sharename}**.
- When you login successful you can work on it like a Linux machine and use t's commands.