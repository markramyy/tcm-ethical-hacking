# A Pentester's Day to Day

---

The day can be performing an **Assessment**, different assessment types, it could be **Writing a Report**, it could be **Giving a Debrief**, or **A Collection of the three** .

![[Pentest's-Day.png | 600 ]]

---

## Types of Assessments

---

### 1. ***External Network Pentest***

---

- It is probably the most common test of pentest that can be preform. 

- It is looking at an organization's security from the outside. This could be us trying to hack in from our mom's basement or from another country or wherever maybe.

---

- The Methodology for external pentests focuses heavily on what's called **Open-Source Intelligence Gathering** ( #OSINT)

-  We're trying to gather as much intel and data about an organization.

- Tends to Last around 32-40 hours on average with another 8-16 for report writing 

---

Now this is the most common type that organization do for 2 reasons.

- Then main reason is a lot of compliance organizations dictate that an external network pentest must be preformed annually, that is not true for the rest of pentest.

- the other side is  it tends to be a little bit cheaper than the rest of the assessments, depending on the size and scope of the engagement and a lot of organizations like to dip their toes in the water before going and doing more assessments with a security firm.

---

### 2. ***Internal Network Pentest***

---

- This is assessing an organization security from the inside of the network. This means that we somehow breached the perimeter.

- Perhaps we sent a phishing email and somebody opened our email, clicked on our link and now we are inside the network. Or maybe we broke into the building and left a Dropbox behind whatever scenario in your head.

---

- What we do in our end is we typically send a laptop out to the client, he plugs that laptop in and we are able to remote into that laptop and preform the Network assessment as if we were sitting inside the office. 

- Now the Methodology for an internal penetration test focuses heavily on active directory

- Tends to Last around 32-40 hours on average with another 8-16 for report writing.

---

### 3. *Web Application Pentest*

---

- Assessing an organization's web application security.

- The Methodology focuses heavily on web-based attacks, obviously, and the Open-Web Application Security Project #OWASP testing guidelines.

- Tends to Last around 32-40 hours on minimum with another 8-16 for report writing 

---

### 4. *Wireless Pentest*

---

- Assessing an organization's wireless network security. 

- The Methodology will vary depending on what type of wireless network is being used.

- If it is a guest network, we might log on to the guest network and test segmentation.

---

- if they're using pre-share key ( #WPA2-PKS), which is common in households, we might test that pre-share key for password strength and see how strong it is.

- If they're using enterprise based network ( #WPA2) then we open ourselves up to a variety of new attacks as well.

- Typically lasts 4-8 hours per #SSID with another 2-4 for report writing.

---

### 3. *Physical Pentest & Social Engineering*

- Assessing an organization's physical security and/or end-user training.

- Methodology depends on task and goals.

- Pure social engineering it means like doing a fishing campaign in combination with an external pen-test.

- Typically lasts 16-40 hours wit another 4-8 for report writing.

---

### 4. Other Assessments

- **Mobile** Penetration Testing  &&  **IoT** Penetration Testing

- **Red** Team Engagements : are kind of like pen testing but the red team is trying to sneak in in whatever creative way you can.

- **Purple** Team Engagements : is something that you might do tabletop exercises and things like that where you as a red team or being offensive and working with a blue team for defensive, that makes you purple.

- And More +++

---

## Report Writing

| A report is typically delivered within a week after the engagement ends | Report should highlight both non-technical (executive) and technical findings | Recommendations for remediation should be clear to both executives and technical staff |
|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|


---

## Debrief

| A debrief walks through your report findings. This can be with technical and non-technical staff present | It gives an opportunity for the client to ask questions and address any concerns before a final report is released. |
|:--------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|


---
