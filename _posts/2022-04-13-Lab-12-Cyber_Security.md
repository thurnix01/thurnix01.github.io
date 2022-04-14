---
layout: post
title:  2022-04-13_Lab 12 - Kenobi - Cyber_Security
---
Week 12 Lab
Kenobi

<img width="988" alt="Screen Shot 2022-04-13 at 10 02 14 PM" src="https://user-images.githubusercontent.com/98490306/163309500-6773e689-3095-49f9-b0ee-bc540e2c8e9a.png">

Task 1:

1.	Make sure you're connected to our network and deploy the machine
 No answer needed

2.	Scan the machine with nmap, how many ports are open?
Answer: 7

Task 2:

3.	Using the nmap command above, how many shares have been found?
Answer: 3

4.	Once you're connected, list the files on the share. What is the file can you see?
Answer: log.txt

5.	What port is FTP running on?
Answer: 21

6.	What mount can we see?
Answer: /var


Lets get the version of ProFtpd. Use netcat to connect to the machine on the FTP port.
7.	What is the version?
Answer: 1.3.5

8.	How many exploits are there for the ProFTPd running?
Answer: 4

9.	We know that the FTP service is running as the Kenobi user (from the file on the share) and an ssh key is generated for that user.
No Answer Needed

10.	We knew that the /var directory was a mount we could see (task 2, question 4). So we've now moved Kenobi's private key to the /var/tmp directory.
No Answer Needed.

11.	What is Kenobi's user flag (/home/kenobi/user.txt)?
Answer: d0b0f3f53b6caa532a83915e19224899

To search the a system for these type of files run the following: find / -perm -u=s -type f 2>/dev/null

12.	What file looks particularly out of the ordinary?
Answer: /usr/bin/menu

13.	Run the binary, how many options appear?
Answer: 3

14.	We copied the /bin/sh shell, called it curl, gave it the correct permissions and then put its location in our path. This meant that when the /usr/bin/menu binary was run, its using our path variable to find the "curl" binary.. Which is actually a version of /usr/sh, as well as this file being run as root it runs our shell as root!
No Answer Needed

15.	What is the root flag (/root/root.txt)?
Answer: 177b3cd8562289f37382721c28381f02
