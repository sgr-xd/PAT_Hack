# PAT_Hack
**Researcher Name:** Guru Raghav Saravanan

**Website:** pat.psgtech.ac.in

**Vulnerability: XSS** via pdf.js library

**Description:**

PDF.js, a popular JavaScript library used for rendering PDFs in web applications, is vulnerable to XSS attacks if it does not properly sanitize the content of the PDFs. This vulnerability allows an attacker to inject arbitrary JavaScript code within a PDF file, leading to the execution of this code when the file is rendered in a user's browser (firefox).

This library is being used in **pat.psgtech.ac.in** which allows me to upload a malicious pdf in the resume section and execute the script of my wish.

**Proof Of Concept:**

I created a malicious pdf and uploaded the resume in the profile’s resume section.

The pdf when opened normally will look simple and neat:


<img src="/assets/ori_pdf.png" width="600" height="400" />

When I upload the above and open it in the pat portal my script gets executed. I have created two pdf:

1. Will display the cookie
2. Will display a Message to the User

**Displaying Cookie:**

<img src="/assets/cookie_pat.png" width="600" height="400" />

**Viewing the pdf by clicking the eye button:**

<img src="/assets/cookie_msg.png" width="600" height="400" />

**Displaying Hacked Message:**

<img src="/assets/hack_msg_pat.png" width="600" height="400" />

**Viewing the pdf by clicking the eye button:**

<img src="/assets/hack_msg.png" width="600" height="400" />

**Conclusion:**

**Impacts of an XSS vulnerability via malicious PDF injection using PDF.js < 4.2.67**

1. Theft of Cookies and Session Tokens: Enables session hijacking.
2. Unauthorized Actions: Allows attackers to perform actions on behalf of the user.
3. Escalation of Privileges: Provides unauthorized access to restricted areas.
4. Drive-by Downloads: Forces victim's browser to download malware.
5. Phishing Attacks: Creates realistic phishing forms to steal credentials.
6. Website Defacement: Alters the appearance of the website.
7. Denial of Service (DoS): Crashes the victim's browser or exhausts system resources.
8. Spread of Worms: Propagates self-replicating scripts across the site.
9. Compromise of Client-Side Storage: Accesses and manipulates local storage data.

**Mitigation:**

1. Update PDF.js to version 4.2.67 or higher
2. Firefox should be updated to > v126)

**Video POC:**

https://github.com/user-attachments/assets/b84926ad-613a-4788-bba6-03cbbf8e16b5



