---
title: Penetration Testing
author: p0i5on
tags: introduction pentesting
aside:
  toc: true
sidebar:
  nav: layouts
mathjax: false
mathjax_autoNumber: false
mermaid: false
chart: false
excerpt_separator: <!--more-->
key: pentesting001
---

## What is Penetration Testing?
[Penetration testing](https://en.wikipedia.org/wiki/Penetration_test) or Pen testing is a security exercise where a cyber-security expert attempts to find and exploit vulnerabilities in a computer system. The purpose of this simulated attack is to identify any weak spots in a system’s defenses which attackers could take advantage of.

This is like a bank hiring someone to dress as a burglar and try to break into their building and gain access to the vault. If the 'burglar' succeeds and gets into the bank or the vault, the bank will gain valuable information on how they need to tighten their security measures.

## Why Penetration Testing?
Penetration is essential in an enterprise and proves its value for organizations looking to:
- Determine the feasibility of a particular set of attack vectors
- Identify higher-risk vulnerabilities resulting from lower-risk vulnerabilities exploited in a particular way
- Highlight vulnerabilities difficult or impossible to detect with automated network or application scanning software
- Assess potential business and operational impacts of successful attacks
- Test network defense's ability to successfully detect and respond to the attack
- Meet compliance requirements
- Implement and validate new security controls put in place to thwart similar attacks in the future.

## Types of Pen Tests
### White box pen test
In a white box test, the hacker is provided with some information ahead of time regarding the target company's security info.

### Black box pen test
Also known as a **blind** test, this is one where the hacker is given no background information besides the name of the target company.

### Covert box pen test
Also known as a **double-blind** pen test, this is a situation where almost no one in the company is aware that the pen test is happening, including the IT and security professionals who will be responding to the attack. For covert tests, it is especially important for the hacker to have the scope and other details of the test in writing beforehand to avoid any problems with law enforcement.

### External box pen test
In an external test, the ethical hacker goes up against the company's external-facing technology, such as their website and external network servers. In some cases, the hacker may not even be allowed to enter the company's building. This can mean conducting the attack from a remote location or carrying out the test from a truck or van parked nearby.

### Internal box pen test
In an internal test, the ethical hacker performs the test from the company's internal network. This kind of test is useful in determining how much damage a disgruntled employee can cause from behind the company's firewall.

## Stages in a Penetration Test
### Scoping - Determine the rules of engagement for the assessment
The project or testing scope agreement, typically included in a Statement of Work with the testing vendor, should cover the high-level testing methodology and the exploitation-depth allowed once vulnerabilities are discovered. Penetration testing is a white hat process, meaning the attacker is a tester playing by rules of engagement determined during scoping. Therefore, the engagement itself should not disrupt normal business operations.

### Reconnaissance - Gathering any information relevant to the assessment goals and enumerating the attack surface
During this next phase, the tester will use various sources to gather as much information about the target as possible, including researching the organization, generating threat intelligence, and enumerating attractive services within the network. An experienced penetration tester will collect information available publicly, called open-source intelligence, as well as general information about systems provided by the enterprise that might also be available in public.

### Vulnerability Assessment - Identifying vulnerabilities and quantifying the risk associated
This phase of the engagement goes deep to identify the vulnerabilities on the target network. The penetration tester will send probes to the target network, collect preliminary information, and then use the feedback to probe for more input and to discover additional details.

The output from this stage can contain the following:
- Directory structure on a specific server
- Open authentication access to some FTP web servers
- Available SMTP access points providing architectural details about the network through error messages
- Remote-code execution possibilities
- Cross-site scripting vulnerabilities
- Internal code-signing certificates that could be used to sign new scripts and inject them into the network

### Exploitation - Actively exploiting vulnerabilites identified
Once a threat model and attack plan have been developed based on the discovered vulnerabilities, the next stage is to penetrate systems in the targeted network. There is no guarantee that every discovered vulnerability will be exploited; there could be a secure network, DMZ, firewall, server, router, or an old system in the network that remains outside the scope of the test.

An experienced penetration tester will focus on vulnerabilities that can be exploited to gain access to the target system. During this phase, the tester is also focused on collecting more in-depth data across the target network.

### Lateral Movement - Maintaining access to the environment and continuing to gain access to data or assets
Once the tester gains access to a system, they will inject agents that maintain access to the system. Maintaining successful access means these agents live in the system and keep that access over a period of time, even if the system is rebooted, reset, or modified by network administrators.

### Artifact Collection/Destruction - Gathering up any accounts, software, or files left behind from testing
The stage following exploitation and maintained access ensures that every exploited system is cleaned after gathering data for the testing report. Cleaning removes all agents, scripts, planted executable binaries, and temporary files, etc.

The clean-up process should ensure that all installed backdoors or rootkits have been removed, and it should return the system configuration to its original, pre-engagement state. Any credentials changed should be restored, and any additional usernames created should be removed.

### Reporting/Debriefing - Communicating the test results
The vendor then submits a report to the client; this report is the tool that will best communicate your pen test results, and the report will target two different groups: business executives and technical teams.

The pen test report should start with an executive summary explaining your penetration test strategy in business terms, identifying results by risk rating. This section should be brief, and it might be the most important piece the client uses to make decisions: the business team will decide what to fix, and which issues represent an acceptable level of risk.

The second part of the report is technical detail, which should be descriptive and specific, avoiding general or vague statements. The technical team will use this part of the report to take action and fix security issues discovered during the penetration test.

## How to get started?
### Hands-on Practice
[TryHackMe](https://tryhackme.com/) is a great platform to start hands-on penetration testing practice right away. Here is a great introductory video on penetration testing by [JohnHammond](https://www.youtube.com/user/RootOfTheNull)

<div>{%- include extensions/youtube.html id='xl2Xx5YOKcI' -%}</div>
<br>

[HackTheBox](https://www.hackthebox.eu/) is another great platform to practice your pentesting skills but there are no writeups for active machines on HTB, writeups are only published after a machine is retired.   

Every Saturday a machine retires at 20:30 IST and a new machine is released 4 hours later at 00:30 IST Sunday. You can access a retired machine for 2 more weeks without a VIP subscription.   
HackTheBox also has jeopardy style CTF challenges and a new challenge is released every Saturday at 00:30 IST.

<div>{%- include extensions/youtube.html id='ZrhyQWYnFFE' -%}</div>

### Ippsec
[Ippsec's](https://www.youtube.com/c/ippsec) youtube channel is probably the best place to learn pentesting. Every saturday when a machine retires on HackTheBox, he publishes a walkthough for it. Not only he shows how to hack a machine very realistically, he also shows the rabbit holes he went into while hacking a machine.

If you want to learn about a topic lets say 'port forwarding', just search it on [ippsec.rocks](https://ippsec.rocks/#) and you will get multiple videos where he explains about that particular topic while hacking a HackTheBox machine.

![](/IITBreachers-wiki/assets/images/pentesting/ippsecrocks.png)

### Resources
Everything you need to know about pentesting is present in [book.hacktricks.xyz](https://book.hacktricks.xyz/)
