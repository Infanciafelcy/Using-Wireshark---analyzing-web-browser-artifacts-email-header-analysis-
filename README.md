# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
Captured Web Activity and Email Header Information
A. Capturing Traffic in Wireshark

Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

Stop the capture once done.

![image](https://github.com/user-attachments/assets/ceb9594a-0e3c-4e02-be08-fb0d1385d8f7)
Analyze DNS Queries: o Filter: dns

o Reveal domains the browser tried to resolve.
![image](https://github.com/user-attachments/assets/dcda7ea6-184a-4c61-ae06-54d03b174dd1)
mail Header Analysis

Apply relevant filters:
o For POP3: tcp.port == 110

o For SMTP: tcp.port == 25 or 587

o For IMAP: tcp.port == 143 or 993

Locate email data:
o Look for SMTP packets to see sender/receiver email addresses.

o Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

Extract Email Header Fields:

o Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

![image](https://github.com/user-attachments/assets/2834b51a-19c8-472d-9790-4658639177d0)
![image](https://github.com/user-attachments/assets/ecd82ed5-5336-4549-8f26-5ffcb55d66aa)
![image](https://github.com/user-attachments/assets/299289e8-caa4-4156-8137-7eccc2e072cc)

## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

