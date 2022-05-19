---
layout: post
title:  2022-05-18_Lab 5 - Mobile Malware Analysis - Cyber_Security
---
Week 5 Lab

<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/169206568-96a006ff-44d3-48cb-a967-828436757108.png">

**Task 1:**
Answer the questions below
Read the text above.
No answer needed

**Task 2:**


1.	What known as the first malware created to affect mobile devices?
Answer: Cabir

2.	What technology does this worm used to multiply?
Answer: Bluetooth

3.	What operating system did it infect?
Answer: Symbian

4.	What message did it show on the screen of the infected mobile phone?
Answer: Caribe

5.	The worm was created and sent out by researchers as a PoC (Proof of Concept), they did not believe that the mobile operating system could be easily exploited. Since then, malicious programs have become more popular. 
Answer: No answer needed



**Task 3:**

6.	Deploy the machine & use MobSF to scan the file named "TWFsd2FyZQ.apk" that is located on the Desktop.
Answer: No answer needed

7.	What is the format of the file?
Answer: .apk

8.	The sample's size is 10,1 bytes, so it seems that it is not a complex application.
Answer: No answer needed

9.	Decode the name of the sample.
Malware

10.	Which is the target platform?
Answer: Android



**Task 4:**

11.	What does Avast-Mobile can tell us about this software?
Answer: Android:Metasploit-Q [PUP]

12.	What program was used to create the malware?
Answer: Metasploit

13.	The results provided by VirusTotal shows that we have a generic malware. It does not serve for attack purposes because we can see that a good part of the Antiviruses are detecting it, this malware is a good one for searching purposes, but it is also used for post exploitation.
Answer: No answer needed

14.	What is the package name?
Answer: com.metasploit.stage

15.	What is the SHA-1 signature?
Answer: 74d442594acf11dc6e3492ffea5eb8956afd000d


16.	By extracting the content, it will create a folder with some files inside, one of which is a XML. It describes some important information about the application for Android build tools, for Android operating system and for Google Play. This file declares items, shows some stuff as the package name and the permissions required to the device. The information that will be needed for the next questions can be found on VirusTotal also.
Answer: No answer needed

17.	What is the unique XML file?
Answer: AndroidManifest.xml 

18.	How many permissions are there inside?
Answer: 22

19.	Which permission allows the application to take pictures with the camera?
Answer: android.permission.CAMERA

20.	What is the message left by the community?
Answer: THM{V1ru5-T0t4al-TWFsd2FyZS1BbmFseXNpcw}



**Task 5:**

21.	What is the programming language used to create the program?
Answer: Java

22.	How many signatures does the package has?
Answer: 1

23.	Application is signed with v1 signature scheme, what is it vulnerable to on Android <7.0?
Answer: Janus

24.	MobSF gives all the code decompiled. Just a base of programming make us able to understand a little bit of what is happening.
Answer: No answer needed

25.	This malware is used to create a connection with the victim that is called a reverse shell.
Answer: No answer needed

26.	What is the App name?
Answer: MainActivity

27.	It looks like there is a function calling for the package manager, so it can see all the installed applications. What function is that?
Answer: b.getPackageManager

Returning to the manifest.

28.	The flag "android:allowBackup" allows the user to backup application data via USB debugging. It is recommended that this be set as "False", even if by default it is "True".
What is the severity of this configuration?
Answer: Medium



**Task 6:**

29.	What is the SHA-256 hash of the file?
Answer: bd8cda80aaee3e4a17e9967a1c062ac5c8e4aefd7eaa3362f54044c2c94db52a

30.	After finding the sample on VirusTotal, what does the "Avast" anti-virus engine recognizes it as?
Answer: Android:Obfus-BM [Trj]

31.	With what we have, try to find out the name of the sample.
Answer: Pegasus

32.	It seems like it is a very dangerous malware and has a big history of destruction.
This became news for spying journalists, what year was that?
Answer: 2017

33.	It was reported that the malware was developed by a legitimate intention:  The idea behind it was to use the software as a government tool designed to track and combat terrorism and crime.

This malware has been found infecting people's smartphones and political activists in more than 44 countries.
Answer: No answer needed

34.	If we search the name we found of the malware in MITRE ATT&CK (https://attack.mitre.org/), we can find some interesting information. 
What is the ID of the MITRE ATT&CK that is associated with our sample?
Answer: S0316

35.	What technique has the ability to exploit OS vulnerabilities to escalate privileges?
Answer: T1404

36.	Now, let's go back to the MobSF analysis.
Answer: No answer needed

37.	There is a permission that when accepted, allows the application to access the list of accounts in the Accounts Service. What is the status shown by MobSF regarding this permission. (android.permission.GET.ACCOUNTS)
Answer: dangerous

38.	What org.eclipse.paho.client file refers to properties of Portuguese from Brazil (pt-br)?
Answer: org/eclipse/paho/client/mqttv3/internal/nls/messages_pt_BR.properties

39.	This software has several features that make the identification and the processes it performs to explore the target, harder to handle, even when it is being analyzed.
Answer: No answer needed


40.	The malware has a special appeal for its safety and its internal components, reducing the risk of compromise. It has a functionality for its cryptographic operations with the feature of a random bit generation service. How can it be identified?
Answer: FCS_RBG_EXT.1.1



**Task 7:**

41.	If you have any feedback, feel free to contact me on discord: farinap5#4535

 Answer the questions below
 Thank you for your participation!

 Answer: No answer needed
