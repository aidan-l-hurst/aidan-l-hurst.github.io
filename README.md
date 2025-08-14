aidan-l-hurst.github.io

### <span class="blue-text">Email: aidan.l.hurst@gmail.com </span>

### <a href="https://www.linkedin.com/in/aidan-hurst-445453303" style="color: blue;">LinkedIn</a>
# Portfolio
## About
I’m an aspiring Information Security Analyst with a strong foundation in IT and 
cybersecurity, gained through formal education, hands-on projects, and industry 
certifications. While I have a long-term interest in compliance, I’m currently 
pursuing entry-level roles such as SOC Analyst, Cybersecurity Analyst, or IT 
Support positions (including Help Desk) that will allow me to further develop 
my skills in threat detection, incident response, and security operations.

### Education
**Associate of Science in Electrical & Computer Engineering**, Bellevue College, 
Graduated Winter 2023 (3.7 GPA)

### Certifications 
**-CompTIA Security+, issuer: CompTIA, Completed July, 2025**

**-Splunk Search Expert 101, issuer: Coursera, Completed July, 2025**

**-Google Cybersecurity Professional Certificate, issuer: Coursera, Completed Fall 2024**

# Cybersecurity Projects 
### Project 1, Malware Detection & Incident Response: 
-Investigated a suspicious file using its SHA-256 hash and VirusTotal OSINT 
(Open-Source Intelligence); documented findings in an incident handler’s journal. Shown below.

**Date:** 07/26/2024

**Description:** This entry is a documentation of an event involving a suspicious file that was downloaded by an employee through an email attachment. 

**Tool(s) used:** IDS, SHA256, Virus Total

**Report:** Today, an email containing a password protected attachment was received by an employee (1:11pm) who then downloaded it (1:13pm). When the employee entered the password, as directed in the email,, the file executed a malicious payload that created multiple unauthorized executable files (1:15pm). The IDS detected this event and sent an alert to the SOC team (1:20pm). An analyst isolated the suspicious file and created a SHA256 hash (shown below) that was then entered into the Virus Total SEARCH option. The report from VirusTotal indicates that the file associated with this hash is almost definitely malware, as 63/75 security vendors flag it as such. The details section indicates the popular threat label (title) for this file as “Flagpro” and is a type of trojan horse malware used by the threat actor BlackTech. Tags in the report bulletin include “checks user input.” A report from a CAPE sandbox reveals multiple indicators of compromise (IOCs): 
1. The executable seems to create additional files containing cookies, possibly for the purpose of collecting sensitive information. 
2. Dropped files (files written to by executable) include JavaScript, possible XSS.
3. Creates a Hidden/System file(s) 

SHA256 Hash: 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b 

**Summary/Additional Notes:** The file is well recognized as a trojan horse type malware by the security community. The fact that the file being studied creates cookies, modifies Java Script files, autonomously performs insecure HTTP requests, and exhibits collection tactics, point to the file possibly being designed to steal sensitive information from users of websites. 

### Project 2, SIEM Querying in Splunk: 
-Used SPL to identify IOCs (Indicators of Compromise) such as failed login attempts 
and impossible travel; developed familiarity with search syntax and detection. Searches shown below in 1-3.

1. Query to access the index, where all events are ingested, stored, and aggregated 
![SPL query 1](assets/img/Splunk%20query%201.png)

2. Searched for failed login attempts to the root user account on the mailsv host. Used
the wildcard fail* to bring up all events containing "fail", "failed", "failure". 
![SPL query 1](assets/img/Splunk%20query%202.png)

3. Practiced the use of booleans such as OR. This query returns events where the host is "mailsv" or where the host is "www1" and contains fail* and root.
To search for failed logins of the root account on both the "mailsv" and "www1" hosts, use the following query: __index=main (host=mailsv OR host=www1) fail* root__ 
![SPL query 3](assets/img/Splunk%20query%203%20OR%20statement.png)


### Project 3, Security Alert Triage: 
-Analyzed a mock security alert ticket using a standard playbook; documented IOCs 
and proposed escalation steps; developed investigation and triage skills. Shown below.

**Date:** 07/28/2024

**Description:** This entry is a documentation of a ticket (id: A-2703) involving a suspicious file believed to be a phishing attempt.

**Tool(s) used:** IDS, SHA256, Virus Total

**Report:** The security team is investigating a medium level ticket alert (id: A-2703). The alert states that on 07/20/2022 at 9:30am, an employee user received an email containing an attachment. The attachment is a file verified to be malicious in nature and was possibly opened by the user. This verification was accomplished by searching the file's respective SHA256 hash on VirusTotal. The ticket shows a number of Indicators of Compromise(IOCs). The email contains a misspelling of the word engineer in the subject line and a mismatch between the sender's name and email address. The sender's email address is akin to that of an organization, suggesting the possibility that they are attempting to impersonate a credible source. Additionally, the sender claims that the attachment is a resume, but the attached file is a executable(.exe) as opposed to a word document or PDF.

**Summary/Additional Notes:** Based on the fact that the attachment is verified to be malicious along with the other IoCs outlined above, this alert/ticket is credible, and should be escalated. 

### Project 4, Risk Assessment and Analysis: 
-Conducted a risk assessment of a fictitious server using NIST SP 800-30 as a guide. Evaluated interfaces, specifications, and identified vulnerabilities, then delivered a report recommending mitigations.

**Risk Assessment:**
Because of the specifications of  the database server, it offers a valuable data storage and retrieval system, with the ability to transport data securely over an SSL connection. This server will likely store sensitive data on customers and possibly employees. Failure to address vulnerabilities and exposures could result in an attack that damages the company's reputation and ability to conduct business. If an attack were to deny access to the data stored server, this would make finding potential customers more difficult, likely slowing growth of the business. If an attacker were to steal data on the server, this could harm customers and in effect our company's reputation.

**Risk Analysis:** 
The server’s public accessibility leaves it vulnerable to unauthorized access by human threats, including: competitors and hackers. Since the company conducts business globally, this could potentially attract the attention of nation-states who may use our server to obtain sensitive information on business partners. The likelihood of this hinges largely on who we do business with and the nature of that business. The severity here is high because, if compromised, we could lose current customers and find them challenging to replace due to reputational damage.

Our remote employees introduce the risk of working on an insecure network (e.g., WPA, WEP) and a threat actor performing an on-path attack. The likelihood of this is based on the hardware used and the risks associated with remote work. The severity here is moderate, predicated on the fact that a single employee is not necessarily accessing a large quantity of sensitive information in a single session. 

Business partners could develop an interest in influencing decisions of our organization in order to put themselves at an advantage. They may access information on this server, that they likely know exists, and monitor our company activities. The risk of this requires a degree of speculation and hinges on who we do business alongside and our relationship with respective organizations. The possible impact is severe.

**Remediation Recommendations:** 
1. To mitigate unauthorized access to the server, implement multi-factor authentication (MFA) for all employees.
2. To reduce the risk of an on-path attack over unsecured networks, require all remote employees to use a VPN when accessing company resources, including the server.
3. To mitigate the risk of unauthorized access, surveillance or influence, use symmetric encryption (AES-256) to protect data at rest while maintaining system performance.

More projects to be added...
