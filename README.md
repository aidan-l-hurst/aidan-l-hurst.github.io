# aidan-l-hurst.github.io
### Email: aidan.l.hurst@gmail.com
### [LinkedIn](https://www.linkedin.com/in/aidan-hurst-445453303 )
# Portfolio
## About
I’m an aspiring Information Security Analyst with a strong foundation in IT and 
cybersecurity, gained through formal education, hands-on projects, and industry 
certifications. While I have a long-term interest in compliance, I’m currently 
pursuing entry-level roles such as SOC Analyst, Cybersecurity Analyst, or IT 
Support positions (including Help Desk) that will allow me to further develop 
my skills in threat detection, incident response, and security operations.

### Education
Associate of Science in Electrical & Computer Engineering, Bellevue College, 
Graduated Winter 2023 (3.7 GPA)

### Certificaitons 
-CompTIA Security+, issuer: CompTIA, Completed July, 2025

-Splunk Search Expert 101, issuer: Coursera, Completed July, 2025

-Google Cybersecurity Professional Certificate, issuer: Coursera, Completed Fall 2024

# Cybersecurity Projects 
1. Malware Detection & Incident Response: 
-Investigated a suspicious file using its SHA-256 hash and VirusTotal OSINT 
(Open-Source Intelligence); documented findings in an incident handler’s journal.

2. SIEM Querying in Splunk: 
-Used SPL to identify IOCs (Indicators of Compromise) such as failed login attempts 
and impossible travel; developed familiarity with search syntax and detection.

2a. Query to access the index, where all events are ingested, stored, and aggregated 
![SPL query 1](assets/img/Splunk%20query%201.png)

2b. Searched for failed login attempts to the root user account on the mailsv host. Used
the wildcard fail* to bring up all events containing "fail", "failed", "failure". 
![SPL query 1](assets/img/Splunk%20query%202.png)

2c. Practiced the use of booleans such as OR. This query returns events where the host is "mailsv" or where the host is "ww1" and contains fail* and root.
To search for failed logins of the root account on both the "mailsv" and "ww1" hosts: index=main (host=mailsv OR host=ww1) fail* root. 
![SPL query 3](assets/img/Splunk%20query%203%20OR%20statement.png)

4. Security Alert Triage: 
-Analyzed a mock security alert ticket using a standard playbook; documented IOCs 
and proposed escalation steps; developed investigation and triage skills.

