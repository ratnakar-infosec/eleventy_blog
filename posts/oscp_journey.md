---
author: Me
title: "My OSCP Journey: Passing the New Pattern of the Exam on the First-Ever Attempt"
date: 2022-03-07
description: A blog describing my OSCP jouney, all the way from knowing about OSCP to passing it.
tags:
 - oscp
 - offensive security
 - active directory
 - cyber security
---

![OSCP Digital Certificate](https://cdn-images-1.medium.com/max/6600/1*1WBXfgLov14fUOM2K9AynQ.jpeg)

### **1. Introduction**

This write-up will be all about my OSCP journey, I’ll try to include every phase of this journey in this article. Please note that any opinion in this article will be my personal opinion that may differ from someone else.

**1.1 whoami /all**

I’m a 21-year-old Information Security Researcher and I completed my schooling from Kendriya Vidyalaya Ambernath (1-12th) in the science stream. Then I pursued BCA (specialized in Cloud Technology and Information Security) from Ajeenkya DY Patil University, Pune. I work as a part-time Subject Matter Expert for Computer Science Engineering. Apart from this, I also like playing online games, sketching, and painting.

**1.2 How it all started?**

I was introduced to OSCP by one of our college professors who also suggested me to actively participate in “Responsible Disclosure Programmes” during their career path session to get familiarize with the field in much more depth. I got so excited by the term “bug bounty” that while every one of us was locked-down during the global pandemic and trying to learn something new, I was busy learning about bug hunting from wherever I could, and results were reflected after several months when I submitted numerous bug reports to various organizations.

**1.3 When it all started?**

Exactly on 25th June 2020, I decided to take OSCP. However, It was so expensive and I never want my family to pay for it so I waited. Fortunately, I got freelancing work as a “Subject Matter Expert” and I also got a few bug bounties that both helped me pay to upgrade my machine, purchase practice labs, and the exam voucher.

### 2. Preparation

**2.1 Passive Preparation I**

The passive preparation journey began just after I decided to take the exam, where I watched infosec videos on YouTube, and read articles about this examination. Whenever someone shares their OSCP journey experience, tips, and preparation guides both via video and writeups, I used to finish them all.

The moment I read the PWK syllabus, I was astonished that “Man! I don’t about any of these except a few”. Then I calmed myself and started learning about those topics from different resources such as writeups, articles, and YouTube videos.
>  In my opinion, The things you’ve learned before purchasing the actual course does matter a lot.

**Courses**

Then, alongside my online college studies and work, I completed the following courses during this preparation phase.

 1. [Web Application Pentesting](https://www.youtube.com/playlist?list=PLLKT__MCUeixCoi2jtP2Jj8nZzM4MOzBL) by TCM

 2. [Practical Ethical Hacking](https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course) Course by TCM

 3. [Python 101 for Hackers](https://academy.tcm-sec.com/p/python-101-for-hackers) by TCM Security

 4. [Linux Privilege Escalation for Beginners](https://academy.tcm-sec.com/p/linux-privilege-escalation) by TCM

 5. [Windows Privilege Escalation for Beginners](https://academy.tcm-sec.com/p/windows-privilege-escalation-for-beginners) by TCM

 6. [Linux Privilege Escalation for OSCP & Beyond!](https://www.udemy.com/course/linux-privilege-escalation/) by Tib3rius

 7. [Windows Privilege Escalation for OSCP & Beyond](https://www.udemy.com/course/windows-privilege-escalation/) by Tib3rius

Linux and bash scripting skills are a must for this examination however, I didn’t follow any specific course for it as I learned it by myself using google during my work as SME. The below course is all you need for learning the necessary amount of Linux skills.

[Linux 101 by TCM](https://academy.tcm-sec.com/p/linux-101)

Apart from these, there is another awesome resource for web application attacks that even has practical labs to practice on. The good part about this resource is that it is free.

[Web Security Academy by PortSwigger](https://portswigger.net/web-security)

**2.2 Passive Preparation II**

For all the post-exam writeups that I read, one thing was common that is, the PWK lab machines would not be sufficient and we should practice on other labs too. I followed the amazing OSCP-like VM list by [NetSecFocus Trophy Room](https://docs.google.com/spreadsheets/u/1/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/htmlview).

I decided to give 2 months to practice lab machines available on different platforms. I purchased a 1-month HTB VIP and completed a total of 60 machines in the first 30 days. Then, I chose OSPG over VunHuB as I heard people saying the OSPG machines are possibly closest to actual exam machines. After completing 61 of the available machines in the next 30 days, I would say that “Yes, they are somewhat too similar to the exam machines but except for a few”. Some of the machines of OSPG are like very tough for beginners and are absolutely out of scope for this certification.

**2022 Update**

In the meantime, while working on OSPG boxes on 1st Dec 2021, I read the news that OffSec has decided to change the exam pattern by adding an Active Directory set in the exam. Now, the exam will be having an AD set (1 DC & 2 Clients) for 40 points and 3 independent machines for 2 points each. It is possible to earn partial points for the independent machines (10 points for the user and 10 points for privilege escalation) however, there are no partial points for the AD set, and either we can score a total of 40 points by exploiting the entire AD chain or we get nothing. Additionally, the bonus points for the lab report had been increased to 10.

Read more at [OffSec’s Official Website](https://www.offensive-security.com/offsec/oscp-exam-structure/https://www.offensive-security.com/offsec/oscp-exam-structure/)

**About AD**

Initially, I was stressed about this change but after a few hours, I calmed myself and realized that this has to happen someday and changes were necessary as it will definitely boost the reputation of the certification. I thought, “earlier we could earn an easy 25 points by mastering Buffer Overflows but now, we could earn easy 40 points by learning AD attacks thoroughly”. Also, nowadays it is essential for one to be well-equipped will AD attack concepts to survive in the infosec field.

**About BoF**

Talking about BoF, I would say that although it is very rare to see a binary vulnerable to stack-based buffer overflow nowadays however it’s always good to learn it. We probably could earn easy 10 points by BoF but “it’s not guaranteed that BoF will be in every exam set”.

**AD Preparation**

After the OSPG practice, I reserved another month to learn Active Directory Attacks and reviewed the AD Attacks section in TCM’s Practical Ethical Hacking Course. After performing all the attacks mentioned in the course. Then, I referred to online resources and started playing with the AD environment that I’d created with the help of the course.
>  In my opinion, “Active Directory Attacks” module of the PWK course and AD section of “Practical Ethical Hacking Course by TCM” is more than enough what you need for this certification.

**2.3 Active Preparation**

**Enrolling**

While enrolling for the exam I was a bit confused about whether I should book for a month or two as I really wanted to complete all of the machines. After some R&D, I decided to purchase a 30 days lab so that I can learn time management as well. Then, I faced another hurdle while enrolling for the course that was, non of my payment methods were supported by OffSec and I started looking for help from my friends. Thankfully, one of my friends had a supported debit card using which I enrolled for the course 15 days in advance of the desired starting date. I would recommend anyone who is looking forward to enrolling, must enroll at least 10 days in advance.

**The PWK Course**

I completed the Videos and pdf guide in 5 days and then I started working on the lab machines with good progress. I completed the entire lab of 75 hosts in 25 days working 14 hours a day that include a mock test as well in which, I dedicated 4 machines from the development department and 1 machine from the public network, with a limit just like the actual exam. I didn’t include any AD set as I was confident about it and the only motive for this was to make sure I could work non-stop. I completed those 5 hosts within 14 hours.

![Completed all the lab machines](https://cdn-images-1.medium.com/max/2000/1*iupkvorjQtBHZCjzmavQMw.png)
>  My personal advise to someone who is looking forward to take this course that some of the the lab machines are inter-connected with each other and hence you must perform the post-exploitation enumeration of all the hosts otherwise you will face difficulty.

**The lab report for 10 bonus points**

As I took only 30 days of the lab, It makes no sense and is neither practical to prepare the lab report. It is too lengthy and I honestly hate making such huge reports.

![](https://cdn-images-1.medium.com/max/2000/1*_ZmjoMdPDsxXoXidqgaKxg.jpeg)

**The Lab Architecture**

The architecture of the PWK lab includes a total of 6 different networks out of which, 5 networks include exploitable hosts and 1 will be dedicated for you to work on. Consider the below diagram, Initially, you have access to the “Student Network” and you can exploit its machines.

Two of the machines from this network will be linked to one host from the “IT Department” and one host from the “Development Department” respectively. You need to pivot to these two networks using those interlinked pivot machines. Then, you can use one of the hosts from the “IT Department” to double pivot into the “Administrative Department”.

Then there is another network “Sandbox” whose step-by-step walkthrough is given in the PWK course and really helps a lot to improve lateral movement techniques.

![PWK Lab Architecture](https://cdn-images-1.medium.com/max/3998/1*V6xITknrpcD5UdVEnBWj2w.png)

### 3. The Exam

**3.1 Scheduling**

I scheduled the exam for 3rd March 2022 at 07:30 AM as I’ll be having the entire day to work and a few hours during the night. This time may vary from person to person but make sure to plan a time at which you can work with maximum productivity. I was lucky enough to get the desired exam time by scheduling the exam just a few days before the desired date. But I would highly recommend that schedule the exam at least 7–10 days prior if you want your desired day and time.

I got a confirmation email after scheduling the exam that contain the numeric portion of my OSID and an MD5 hash. These are the credentials to log in at the proctoring software on the exam day.

**3.2 Exam strategy**

My strategy for the exam was to hit the AD set first as I haven’t prepared the lab report. Then working with the independent machines. Once I get passing marks, I’ll take a break and start working on the other 30 points.

**Setting up the exam workstation**

I used kali’s .zshrc bash script to create short aliases for frequently used commands during my passive preparation phase to save time during the exam. And, created a directory that had all the required tools in a hierarchical manner. Just before the exam, I created 5 workspaces, 1 for the entire AD set, 3 for the independent targets, and 1 for the VPN connection and Exam Control Panel so that everything will be neat and nothing gets messed up.

![](https://cdn-images-1.medium.com/max/2000/1*Uh66y5-49bhH-TtX7ew2jw.png)

I also prepared quick reference notes in OneNote and an Excel sheet for all the practice machines during the passive preparation phase so that I can copy the commands easily from the notes in case I forget any command syntax. The Excel sheet has everything about all the boxes I did during the passive preparation phase. It had columns for box name, platform, steps to compromise it, what it was all about, and any special point to keep in mind. I created it thinking that I can quickly refer to it if I encounter any relatable situation.

**Host Compromise Proof Screenshot**

After successful exploitation of a system and obtain a shell on it, I displayed the content of each of the flags, current user, hostname, and IP configuration in the shell and took a snapshot of it.

Linux: *cat /home/USER/local.txt && cat /root/proof.txt && whoami && hostname && ip addr*

![Proof Screenshot in Linux](https://cdn-images-1.medium.com/max/2072/1*sKPWOzElcLsNG66HjL6lNw.png)

Windows: *type C:\Users\USER\Desktop\local.txt & type C:\Users\ADMIN-USER\Desktop\proof.txt & whoami & hostname & ipconfig*

![Proof Screenshot in Windows](https://cdn-images-1.medium.com/max/2124/1*TBNmvDsUih4nnV3e6xPo2w.jpeg)

**3.3 The Exam Day**

**Proctoring**

On exam day, I woke up about 1 and a half hours before to get fresh and set up my workstation. Exactly at 07:15 AM, I logged in to the proctoring software using my OSID and the MD5 hash. The proctor instructed me to show my government ID in the camera but It wasn’t focusing so I had to show him the scanned copy of it, that I had on my system. Then he told me to focus my face on the camera for matching it to the ID and finally I had to give him a tour of the entire room including each corner and my working desk.

**AD Set**

I performed a light port scan for the top 100 ports for each of the 3 hosts and successfully identified the role of each of them and the possible initial target. After an interaction with that host, I found a possible attack vector that I was sure about. I started performing the required attack and successfully gained a foothold on it within 25 minutes.

Then I performed lateral movement techniques eventually compromising the domain controller alongside escalating my privileges on each target at the end of 3 hours and 30 minutes.

After obtaining a shell on each of the hosts, I took a proof screenshot and left the working space as it is, and went for a 15-minute break.

**Target 1**

Performed a light port scan on the target and started looking for possible attack vectors. After 15 minutes, found that the vector was in front of my eyes and I was overlooking it. So, exploited it to gain a user shell on the system within 15 minutes. Then started looking for any privilege escalation vector but found nothing even after 2 hours and 15 minutes so decided to skip the host for now and move to target 3.

**Target 3**

Scanned this host for open ports and found the possible attack vector within 20 minutes in spite of the presence of many rabbit holes may be due to enough practice. Exploited the vulnerability and gained a user shell on the system within 30 minutes. Then took a lunch break and returned after 40 minutes and started working on it again. Within 50 minutes, got a system shell on the host and took the root access proof snapshot, this box took around in about 1 hour and 50 minutes including breaks. Now, as I have 70 points in have and I’m in a safe zone, took a 45-minute break to freshen up my mind and started working on target 2.

**Target 2**

Performed a heavy port scan and was lucky enough to find a vulnerability that I’d encountered before. There were rabbit holes too but as I already knew about the exploit from somewhere else, my mind forced me to focus on it. Exploited that vulnerability and got a user shell on the system within 15 minutes. While looking for any privilege escalation vector, found nothing for the next 1 hour and 25 minutes so decided to take a half-hour break. Then again, started working on it and was able to get a system shell on the box in the next 3 hours followed by taking a system-proof snapshot. So, this box took around 5 hours and 15 minutes including breaks and I had 90 points in hand. So, took a break for an hour for dinner and a small walk.

**Back on Target 1**

Started working on the privilege escalation of this target but found nothing even after 8 hours and 45 minutes so. I tried every possible technique I’d learned but found not even a single attack vector that I could try to exploit. So, rechecked everything including the snapshots, flag submissions, and notes then ended the exam after 24 hours and 45 minutes.

I wish I could have exploited the remaining part as well but later I realized that it has to happen to teach me a lesson that there is always a scope for further improvement. The good thing is that I kept on trying till the very moment ended with no sleep.

**Exam Timeline**

![The Exam Timeline](https://cdn-images-1.medium.com/max/2560/1*PKWJdqINnf-Kpf52ufqD_Q.jpeg)

**3.4 Report writing**

After finishing the exam, I took a break for a few hours then slept for around 4 hours, and then started working on the report. Using “OffSec’s Official Exam Report Template” and consuming around 6 hours, I created the report including the scan results, vulnerability explanation, its fix, exploitation steps, and all the relevant snapshots. Once I exported the report in PDF format, It was looking so good man I cannot tell. For this reason, I would suggest using OffSec’s official Exam Report Template.

I submitted the exam report at around 03:30 AM following the necessary procedure and then slept for a long.

**3.5 The Result Day:**

Exactly after 24 hours and 16 minutes after submitting the report, I got the confirmation email from OffSec that I’d successfully obtained the OSCP certification.

![Exam Result Email](https://cdn-images-1.medium.com/max/2234/1*WcBFO4NDdpYW4GGyttEXUQ.png)

### 4. Miscellaneous

**4.1 Metasploit usage**

During my entire phase of passive preparation, I avoided using Metasploit. But in-case, if I had to use it, I made sure to understand the exploitation steps and tried to repeat it manually if I could.

During the exam, I never encountered any such situation in which I had to use it. The moment when I was stuck on the privilege escalation of the first target, I could have used Metasploit but unfortunately, I didn’t find even a single attack vector.

Just to clarify the Metasploit usage in the exam, we can use the below 4 modules as much as we want.

 1. multi handler (aka exploit/multi/handler)

 2. msfvenom

 3. pattern_create.rb

 4. pattern_create.rb

However, anything apart from these can be used multiple times on only one target. Once we launched Metasploit for a machine, it will be considered as usage no matter if the exploitation was successful or not.

**4.2 Tips**

 1. While practicing on the lab machines, it is ok to look at the walkthrough but just make sure you’ve tried enough by yourself first and every time you look at the walkthrough, make sure you learn something new and add it to your notes.

 2. Create notes by yourself in a way you are comfortable and make sure that is structured such that it saves your time as well.

 3. While working on machines during practice as well as in the exam if you’re not getting any progress even after 2–3 hours then just leave your desk for a while and come back with a different perspective. It really helps a lot trust me on this, I almost stuck badly on the AD then this one saved me there like an angel.

 4. Keep a good energy drink, coffee, tea, or whatever gives you instant energy with you during the exam as the fatigue will start slowing you down.

 5. Keep things as simple as you can in the exam and look for low-hanging fruits first.

### 5. Credits

I would like to thank my family to support me during this journey. When I told them about this certification, they were like if you feel like doing it then just go for it.

Then, I’m also thankful to our college professors and mentors one of who introduced me to this certification and also motivated me in this field.

And most importantly my friends who joined me on this journey, I learned a lot from them and their respective expertise.

Several other OSCP-certified people supported me in this journey in by sharing their experiences and giving great tips.

### 6. Final words

Don’t stress about the exam, just do your job with 100% honesty considering it a task given to you by the lord. The exam is just another in that lab with certain time-limit, restrictions, and conditions where all the machines are intentionally vulnerable to some kind of exploit, you just need to identify them.

#### Some Amazing Resources
- [How I Passed OSCP with 100 points in 12 hours without Metasploit in my first attempt](https://infosecwriteups.com/how-i-passed-oscp-with-100-points-in-12-hours-without-metasploit-in-my-first-attempt-dc8d03366f33)
- [What to Expect From the New OSCP Exam | Offensive Security](https://www.offensive-security.com/offsec/what-to-expect-new-oscp-exam/)
- [Post-OSCP Writeup](https://rizemon.github.io/posts/oscp-reflection/)