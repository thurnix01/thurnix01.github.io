---
layout: post
title: Lab 05 - Active Reconnaissance
---
Week 5 Lab
Active Reconnaissance

Task 2 - Web Browser:

After inspecting the https://static-labs.tryhackme.cloud/sites/networking-tcp/, on Google chrome, I went through the elements in the html to find the elements used on the page. Using the inspection tool   I hovered over the elements available on the page. I found that both Alice and Bob had Questions,  and found that that there is a script entry at the bottom of the html code.

 <img width="402" alt="image" src="https://user-images.githubusercontent.com/98490306/156907322-78a131e5-f22b-4125-a250-605b16cfe520.png">



Script files usually have Event Listeners that are triggered. 

<img width="337" alt="image" src="https://user-images.githubusercontent.com/98490306/156907330-c714b737-acbf-4e27-9006-684f0791d811.png">

 

Navigating to this section on the browser I noticed that the questions were listed under  
“2: Script…”. Expanding this section, I found that there were 8 questions in total.


<img width="468" alt="image" src="https://user-images.githubusercontent.com/98490306/156907333-bf8ac914-6c0f-4b32-a79f-4b57feafe2a0.png">



Starting up terminal on Attackbox looked like this when opening it. And then when using the ping 10.10.179.231 , then it provided me with these details.


Using the man ping option, I was able to find the option to set the size of the data carried by the ICMP echo request?

ICMP size is 8 bytes

Y

Using ping -c limits the ping replies to 10 only – 10
The last IP address of the last router/hop before reaching tryhackme.com is:

172.67.69.208

The IP address of the last router/hop before reaching tryhackme.com is:

104.26.11.229


The amount routers are between the two systems In Traceroute B is:

26

What is the name of the running server?
Apache


What is the version of the running server (on port 80 of the VM)?

2.4.10

Start the VM and open the AttackBox. Once the AttackBox loads, use Netcat to connect to the VM port 21. What is the version of the running server?


0.17
