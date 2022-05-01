---
layout: post
title:  2022-04-30_Lab 14 - Crack the hash 2 - Cyber_Security
---
Week 14 Lab

Crack The Hash Level 2
 Start AttackBox
Advanced cracking hashes challenges and wordlist generation

<img width="985" alt="Screen Shot 2022-04-30 at 8 43 58 PM" src="https://user-images.githubusercontent.com/98490306/166133513-61802f89-896f-41d5-87a9-7a5417cb761d.png">

 

Task 1:

Join Room

Task 2:

1.	Haiti is a CLI tool to identify the hash type of a given hash. Install it.	
Answer: No Answer needed

2.	Launch Haiti on this hash:  741ebf5166b9ece4cca88a3868c44871e8370707cf19af3ceaa4a6fba006f224ae03f39153492853 - What kind of hash it is?
Answer: RIPEMD-320

3.	Launch Haiti on this hash:
1aec7a56aa08b25b596057e1ccbcb6d768b770eaa0f355ccbd56aee5040e02ee
What is Keccak-256 Hashcat code?
Answer: 17800

4.	What is Keccak-256 John the Ripper code?
Answer: raw-keccak-256

Task 3:

RockYou is a famous wordlist contains a large set of commonly used password sorted by frequency.
To search for this wordlist with wordlistclt run:
wordlistctl search rockyou
 	Answer: No Answer needed

5.	Which option do you need to add to the previous command to search into local archives instead of remote ones?
Answer: -l

Download and install rockyou wordlist by running this command: wordlistctl fetch -l rockyou

Answer: No Answer Needed


6.	If you run wordlistctl search -l rockyou one more time, what is the path where is stored the wordlist?
Answer: /usr/share/wordlists/passwords/rockyou.txt
7.	What is the name of the first wordlist in the usernames category?
Answer: CommonAdminBase64

Task 4:


Depending of your distribution, the John configuration may be located at /etc/john/john.conf and/or /usr/share/john/john.conf. To locate the JtR install directory run locate john.conf, then create john-local.conf in the same directory (in my case/usr/share/john/john-local.conf) and create our rules in here.
Answer: No Answer Needed


Let's use the top 10 000 most used password list from SecLists (/usr/share/seclists/Passwords/Common-Credentials/10k-most-common.txt) and generate a simple border mutation by appending all 2 digits combinations at the end of each password.
Let's edit /usr/share/john/john-local.conf and add a new rule:

[List.Rules:THM01]
$[0-9]$[0-9]
Answer: No Answer Needed

8.	
Now let's crack the SHA1 hash 2d5c517a4f7a14dcb38329d228a7d18a3b78ce83, we just have to write the hash in a text file and to specify the hash type, the wordlist and our rule name. john hash.txt --format=raw-sha1 --wordlist=/usr/share/seclists/Passwords/Common-Credentials/10k-most-common.txt --rules=THM01
What was the password?
Answer: moonligh56






Task 5:


Let's say we know the password we want to crack is about dogs. We can download a list of dog races wordlistctl fetch -l dogs -d (/usr/share/wordlists/misc/dogs.txt). Then we can use Mentalist to generate some mutations.
Answer: No Answer Needed

 
Then we can process and save the newly generated wordlist.
It's also possible to export John/Hashcat rules.
Answer: No Answer Needed




9.	Crack the following md5 hash with the wordlist generated in the previous steps.
ed91365105bba79fdab20c376d83d752
Answer: mOlo$$u$



Now let's use CeWL to generate a wordlist from a website. It could be useful to retrieve a lot of words related to the password's topic.
Answer: No Answer Neede

10.	For example to download all words from example.org with a depth of 2, run:
cewl -d 2 -w $(pwd)/example.txt https://example.org
The depth is the number of link level the spider will follow.
What is the last word of the list?
Answer: information


With TTPassGen we can craft wordlists from scratch. Create a first wordlist containing all 4 digits PIN code value.
ttpassgen --rule '[?d]{4:4:*}' pin.txt
Answer: No Answerned


Generate a list of all lowercase chars combinations of length 1 to 3.
ttpassgen --rule '[?l]{1:3:*}' abc.txt
Answer: No Answer Needed 

hen we can create a new wordlist that is a combination of several wordlists. Eg. combine the PIN wordlist and the letter wordlist separated by a dash.
ttpassgen --dictlist 'pin.txt,abc.txt' --rule '$0[-]{1}$1' combination.txt
Be warned combining wordlists quickly generated huge files, here combination.txt is 1.64 GB.
$ wc pin.txt 
10000 10000 50000 pin.txt

$ wc abc.txt 
18278 18278 72384 abc.txt

$ wc combination.txt 
 182780000  182780000 1637740000 combination.txt

Answer: No Answer Needed

11.	Crack this md5 hash with combination.txt.
e5b47b7e8df2597077e703c76ee86aee
Answer: 1551-li

Task: 6
12.	Advice n°1 b16f211a8ad7f97778e5006c7cecdf31
Answer: 

13.	Advice n°2 7463fcb720de92803d179e7f83070f97
14.	Answer: 

15.	Advice n°3 f4476669333651be5b37ec6d81ef526f
16.	Answer: 



17.	Advice n°4 a3a321e1c246c773177363200a6c0466a5030afc
18.	Answer: 

19.	Advice n°5 d5e085772469d544a447bc8250890949
20.	Answer: 


21.	Advice n°6 377081d69d23759c5946a95d1b757adc
22.	Answer: 

23.	Advice n°7 ba6e8f9cd4140ac8b8d2bf96c9acd2fb58c0827d556b78e331d1113fcbfe425ca9299fe917f6015978f7e1644382d1ea45fd581aed6298acde2fa01e7d83cdbd
24.	Answer: 


25.	Advice n°8 9f7376709d3fe09b389a27876834a13c6f275ed9a806d4c8df78f0ce1aad8fb343316133e810096e0999eaf1d2bca37c336e1b7726b213e001333d636e896617
26.	Answer: 


27.	Advice n°9 $6$kI6VJ0a31.SNRsLR$Wk30X8w8iEC2FpasTo0Z5U7wke0TpfbDtSwayrNebqKjYWC4gjKoNEJxO/DkP.YFTLVFirQ5PEh4glQIHuKfA/
28.	Answer: 



