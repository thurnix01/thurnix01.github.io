---
layout: post
title:  2022-05-07_Lab 15 - Investigating Windows - Cyber_Security
---
Week 15 Lab


<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274785-daf5d055-e27f-47f8-966c-d553b9ec737a.png">


1.	What’s the version and year of the windows machine? 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274806-b6127598-b24b-4172-b310-310572798cdc.png">

Answer: Windows Server 2016


2.	Which user logged in last!

<img width="419" alt="image" src="https://user-images.githubusercontent.com/98490306/167274811-1f70f70b-559d-4c60-bd6d-48c75ddd0398.png">

Answer: Administrator


3.	When did John log onto the system last? 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274829-5ce40ff9-13c9-45b2-9086-95e89e57bb1f.png">

Answer: 03/02/2019 5:48:32 PM



I ran “regedit” to navigate to the UpdateSvc file located in HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run

<img width="302" alt="image" src="https://user-images.githubusercontent.com/98490306/167274835-037ef52f-664c-4cca-90d6-2b922a4acc55.png">
4.	What IP does the system connect to when it first starts!

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274842-cc6021d4-39fe-4076-b4bd-3128c5bf8e75.png">

Answer: 10.34.2.3


Using the navigation through Control Panel> System and Security> Administrative Tools> Computer Management

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274846-a4435d6e-f94b-40a2-9510-864ff3e368af.png">

I found the two accounts the also had administrative privileges: Local Users and Groups> Groups> Administrators :

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274853-89d2b6b0-185b-4639-a547-3ecc2d18f130.png">
5.	What two accounts had administrative privileges (other than the Administrator user)!

<img width="323" alt="image" src="https://user-images.githubusercontent.com/98490306/167274865-4c1bc590-0513-4908-a1b1-96f9b7134bad.png">

Answer: Jenny, Guest



6.	What’s the name of the scheduled task that is malicious?
Answer: Clean file system

7.	What File was the task trying to run daily?
Answer: nc.ps1

8.	What port did this file listen locally for?
Answer: 1348


Using the “net user Jenny” command in cmd.exe, I found that she never logged on.

<img width="315" alt="image" src="https://user-images.githubusercontent.com/98490306/167274869-df6be26d-b0fb-47d3-a160-34ed291f1c0e.png">

9.	When did Jenny last logon:
Answer: never

10.	At what date did the compromise take place?
Answer: 03/02/2019

11.	At what time did Windows first assign special privileges to a new logon?
Answer: 03/02/2019 4:04:49 PM


After looking up the Task that was running I found that the event “GameOver” was running through a “mim.exe” file. 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274873-ddba7a4f-6027-495c-92fb-161e2795a2e4.png">

I was not too familiar with the application “mim.exe” so I looked it up and found some useful info in this site: https://www.joesandbox.com/analysis/219878/0/html

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274875-13730819-2d04-4762-98f4-a92bb7e9a3d0.png">

12.	What tool was used to get Windows Passwords?
Answer: Mimikatz

13.	What was the attacker’s external control and command servers IP?
76.32.97.132


I was able to find this info in C:\inetpub\wwwroot

<img width="301" alt="image" src="https://user-images.githubusercontent.com/98490306/167274883-e3b3c21d-d0e8-4afd-9fd4-c5a46a030fbd.png">

 

14.	What was the extension name of the shell uploaded via the server’s website?
Answer:  .jsp

Windows Firewall with Advanced Security stores all Inbound Rules:

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/167274886-a4a077c6-0e7d-4506-bf11-a912f0f8cef0.png">


15.	What was the last port the attacker opened!
Answer: 1337


I was able to find this info in C:\Windows\System32\drivers\etc\hosts

<img width="398" alt="image" src="https://user-images.githubusercontent.com/98490306/167274889-d611b4d2-1aff-460e-bdd5-de1714e5984a.png">

16.	Check for DNS poisoning, what site was targeted:
Answer: google.com


