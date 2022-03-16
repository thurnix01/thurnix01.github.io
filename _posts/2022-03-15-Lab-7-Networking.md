---
layout: post
title: 2022-03-15-Lab 07 - Wifi Hacking 101 - Networking
---
Week 7 Lab

Wifi Hacking 101

Task1 
What type of attack on the encryption can you perform on WPA(2) personal?
•	Answer: Brute Force

 <img width="734" alt="Screen Shot 2022-03-15 at 5 04 45 PM" src="https://user-images.githubusercontent.com/98490306/158497287-a3e0fe73-ab64-4d9b-8bbd-be1d357cc101.png">



Can this method be used to attack WPA2-EAP handshakes? (Yea/Nay)
•	Answer: Nay (this will not work)


What three letter abbreviation is the technical term for the "wificode/password/passphrase" ?
•	Answer: PSK
<img width="763" alt="Screen Shot 2022-03-15 at 5 13 43 PM" src="https://user-images.githubusercontent.com/98490306/158497322-1f06ef4b-53e4-49e0-a979-bdb85834e64c.png">

 


What's the minimum length of a WPA2 Personal password?
Answer: 8

https://www.juniper.net/documentation/en_US/junos-space-apps/network-director4.0/topics/concept/wireless-wpa-psk-authentication.html

<img width="569" alt="Screen Shot 2022-03-15 at 5 17 35 PM" src="https://user-images.githubusercontent.com/98490306/158497236-0a49ad7a-9374-44f6-854e-f38269e7e307.png">


Task2
How do you put the interface “wlan0” into monitor mode with Aircrack tools? (Full command)
•	Answer: airmon-ng start wlan0

 <img width="722" alt="Screen Shot 2022-03-15 at 5 39 11 PM" src="https://user-images.githubusercontent.com/98490306/158497362-385a4179-044d-49e9-9ca6-0d3a38331ba1.png">


And then “wlan0”


What is the new interface name likely to be after you enable monitor mode?
•	Answer: wlan0mon

What do you do if other processes are currently trying to use that network adapter? 
•	Answer: airmon-ng check kill

<img width="727" alt="Screen Shot 2022-03-15 at 5 48 48 PM" src="https://user-images.githubusercontent.com/98490306/158497389-3900fc56-e079-4634-8c61-e17e3b350229.png">

 

What tool from the aircrack-ng suite is used to create a capture?
•	Answer: airodump-ng


What flag do you use to set the BSSID to monitor?
•	Answer: --BSSID


And to set the channel?
•	Answer: --channel




And how do you tell it to capture packets to a file?
•	Answer: -w



 Task 3:

What flag do we use to specify a BSSID to attack?
•	Answer: -b


What flag do we use to specify a wordlist?
•	Answer: -w


How do we create a HCCAPX in order to use hashcat to crack the password?
•	Answer: -j


Using the rockyou wordlist, crack the password in the attached capture. What's the 
password?
•	Answer: greeneggsandham



Where is password cracking likely to be fastest, CPU or GPU?
•	Answer: GPU

