#  Users and Privileges

---

- We run the code **ls -all** :

![[All Files cmd.png | 500 ]]

---

- The First Column tells us :
	1. Whether we are looking at a Directory (if we see d in the beginning) or File.
	2. **rwx** ==> read, write, execute. When one is missing then it can operate its function
	3. There are 3 groups, First **rwx** which is for the owner of the file, Second **rwx** which is for group membership, Last **rwx** which is for all users.

Note: we can use the /tmp folder to upload malware or write a malicious file bc it has the ideal permissions.

---

- We use **chmod** (change mod) to change the privileges of a file (rwx):

	1. chmod +**rwx** (r,w,x depends on need) {file name} ==> for the owner permissions.
	
	2. chmod 777 {file name} ==> it makes every permission available (rwx-rwx-rwx). 

---

- Every number refers to a specific permission :

| ***Number*** | ***Permissions*** | ***Totals*** |
|:------------:|:-----------------:|:------------:|
|      0       |       - - -       |  0 + 0 + 0   |
|      1       |       - - x       |  0 + 0 + 1   |
|      2       |       - w -       |  0 + 2 + 0   |
|      3       |       - w x       |  0 + 2 + 1   |
|      4       |       r - -       |  4 + 0 + 0   |
|      5       |       r - x       |  4 + 0 + 1   |
|      6       |       r w -       |  4 + 2 + 0   |
|      7       |       r w x       |  4 + 2 + 1   |

