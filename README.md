# Hackthebox-Cap-Walkthrough
New Machine and Very Easy Hackthebox Cap CTF Walkthrough


Hello Hacker!
Today I'll Walkthrough most easy and piece of cake ctf CAP

Let's Start

LEVEL- Very Easy


# Reconnaissance

I search on NMAP(Network Mapper), I have found some open ports,

file:///home/aptitude/Pictures/text2image_L5583115_20211008_182356.jpg![image](https://user-images.githubusercontent.com/73866723/136608758-26af9d1e-ca7a-4480-be3a-e1dd02962430.png)

# Enumeration
Then after I using Dirb tool to find Vulernerability

![image](https://user-images.githubusercontent.com/73866723/136609841-264cc009-f3f1-47db-b194-115893c1fa48.png)

When I search on <ip>/data
I found PCAP(Wireshark extenstion file) file in <ip>/data/0 url, when i open this file in wireshark I found many ftp and ssh username and their password.

![image](https://user-images.githubusercontent.com/73866723/136611158-eef38e7a-386d-4216-994f-41a65653bea7.png)

  
# Priviliege Escalation
 
 I login through SSH and I find user.txt file in nathan folder.
 
 After some time, Then we enumerate the target and see that this machine is root previliege of Python3.8
        
 Then I open Python in this machine and using this command
        import os
        os.setuid(0)
        os.system("/bin/bash")
 
then BOOM!
I found root.txt file and finally go to bed.:)
        
        
Thanks You!

Enjoy



