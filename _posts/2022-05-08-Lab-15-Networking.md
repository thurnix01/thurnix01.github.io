---
layout: post
title: 2022-05-08-Lab 15 - Nessus - Networking
---
Week 15 Lab

Nessus
<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167326583-f29e4ae5-b109-4b02-a506-bf09a7918b5f.png">

Tasks 1 and 2 did not require me to do much other than installing the program.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167326603-860bfb00-3c1b-4087-8edf-ad0a80ee3782.png">


Task 3 - Navigation and Scans

1.	What is the name of the button which is used to launch a scan?
Answer:  new scan


2.	What side menu option allows us to create custom templates?
Answer:  Policies

3.	What menu allows us to change plugin properties such as hiding them or changing their severity?
Answer:  Plugin Rules

4.	In the 'Scan Templates' section after clicking on 'New Scan', what scan allows us to see simply what hosts are alive?
Answer:  Host Discovery

5.	One of the most useful scan types, which is considered to be 'suitable for any host'?
Answer:  Basic Network Scan


6.	What scan allows you to 'Authenticate to hosts and enumerate missing updates'?
Answer:  Credential Patch Audit

7.	What scan is specifically used for scanning Web Applications?
Answer:  Web Applications Tests


Task 4 - Scanning!

8.	Create a new 'Basic Network Scan' targeting the deployed VM. What option can we set under 'BASIC' (on the left) to set a time for this scan to run? This can be very useful when network congestion is an issue.
Answer:  Schedule

9.	Under 'DISCOVERY' (on the left) set the 'Scan Type' to cover ports 1-65535. What is this type called?
Answer:  port scan (all ports)

10.	What 'Scan Type' can we change to under 'ADVANCED' for lower bandwidth connection?
Answer:  Scan low bandwidth links

11.	With these options set, launch the scan.
Answer:  No answer needed

12.	After the scan completes, which 'Vulnerability' in the 'Port scanners' family can we view the details of to see the open ports on this host?
Answer:  Nessus Syn Scanner

13.	What Apache HTTP Server Version is reported by Nessus?
Answer:  2.4.99

Task 5 - Scanning a Web Application!

14.	What is the plugin id of the plugin that determines the HTTP server type and version?
Answer:  10107

15.	What authentication page is discovered by the scanner that transmits credentials in cleartext?
Answer:  login.php

16.	What is the file extension of the config backup?
Answer:  .bak

17.	Which director contains example documents? (This will be in a pho directorv)
Answer:  /exernal/phoids/0.6/docs/examoles

18.	What vulnerability is this application susceptible to that is associated with X-Frame Options?
Answer:  ClickJackina

Done!
