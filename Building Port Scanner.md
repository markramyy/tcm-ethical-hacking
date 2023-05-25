# Building Port Scanner
---

```python
import sys
import socket
from datetime import datetime

#Define ot target
if len(sys.argv) == 2 :
	target = socket.gethostbyname(sys.argv[1]) #Translate hostname to IPv4
else :
	print("\t" + "Invalid amount of arguments.")
	print("\t" + "Syntax : python3 scanner.py <ip>")
	
#ADD a banner
print("-" * 57)
print("\t" + "Scanning target : " + target)
print("\t" + "Time started : " +str(datetime.now()))
print("-" * 57)

try:
	for port in range(50,85):
		s = socket.socket(socket.AF_INET , socket.SOCK_STREAM)
		socket.setdefaulttimeout(1)
		result = s.connect_ex((target,port))
		if result == 0 :
			print ("Port {} is open.".format(port))
			s.close()

except KeyboardInterrupt :
	print("\n Exiting program.")
	
except socket.gaierror :
	print("Hostname could not be resolved.")
	sys.exit()
	
except socket.error :
	print("Could not connect to server.")
	sys.exit()

```
