
# Services

---

- We may have a service like a web server or SSH, or maybe an SQL or some sort of database that we need to start while we are already running Kali.

- We might want to start a service , on boot every single time that our computer loads.

- We're gonna look at how to start a service and how to have a service start on launch. 

---

## Start/Stop Service

---

- So the first service that we're going to look at is the **Apache** service (WHY??). The reason is that we can spin up our own web server fairly easily and host malicious data or files or things that we might want to access or might want somebody else to access.

---

- We can start the service using command : "**sudo service apache2 start** "

- And stop it using similar command : "**sudo service apache2 stop**".

---

![[Service-start.png| 600 ]]

---

- We can also use Python to spin up a web server using a command in a file : 
					**python3 -m http.server 80**

- What's gonna happen is any file within the directory that i'm in is gonna now be hosted. It's a quick way to host up a web server without having to start and stop services and you can on the fly within a folder, just start a web service.

---

![[Python-service.png| 600 ]]

---

- Let's say that we wanted a service to start when we started our machine. For that we are going to use the command : " **sudo systemctl enable {ssh}** ".

- When we restart our machine SSH will always be enable for us.

- So if you ever have a service that you want to run, you just need to figure out the name of the service and enable that. And there may be times that you want things to run.