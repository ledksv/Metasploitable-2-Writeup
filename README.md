Metasploitable 2 – Vulnerable Machine Writeup

Platform: Metasploitable (VM)
Type: Intentionally Vulnerable Training Machine

Introduction

Metasploitable 2 is one of the most widely used intentionally vulnerable machines for learning penetration testing. Since this machine is designed specifically for practice, it contains many well-known vulnerabilities across multiple services.

This was my second major lab after completing MR. Robot, and it helped me understand how different attack surfaces work and how insecure configurations can lead to full system compromise.

This writeup provides a high-level overview of my approach.

Initial Enumeration

I began by scanning the machine to identify open ports and running services. Metasploitable 2 intentionally exposes many services, giving a broad attack surface.

During enumeration, I identified:

Web services

FTP

SSH

Database services

Outdated web applications

RPC services

Multiple intentionally misconfigured applications

This machine is purposely insecure, so almost everything you discover becomes a potential point of entry.

Exploring Services

After identifying the available services, I explored each one to understand how they were configured. Many of them were running with default credentials or outdated versions that are known to be exploitable.

A few examples of what I focused on:

A web application vulnerable to simple injection attacks

A service using insecure authentication

An outdated application version with public exploits

Misconfigured directory permissions

An intentionally exposed database

Each of these vulnerabilities became a stepping stone for deeper access.

Gaining Initial Access

The first foothold was achieved by targeting one of the most obviously misconfigured services. Since Metasploitable 2 is designed for training, the initial access is much easier compared to real CTF machines.

Once I gained limited access, I was able to interact with the system and continue exploring internally.

This step taught me the importance of recognizing default credentials, outdated software, and insecure service setups — all common real-world issues.

Privilege Escalation

After obtaining user-level access, I moved on to checking the system for privilege escalation paths:

Reviewing file permissions

Checking running processes

Inspecting installed tools

Examining configuration files

Identifying services running with elevated privileges

Because Metasploitable 2 is intentionally vulnerable, there are multiple ways to escalate privileges. I used one of the simpler ones to gain full control.

This phase helped me understand typical privilege escalation patterns found in Linux systems.

Final Access

With elevated privileges, I was able to explore the full file system and confirm complete control over the machine.

The “final objective” here wasn’t a flag — unlike CTFs — but rather to fully compromise the machine and understand how each layer of its security weaknesses contributed to the overall vulnerability.

What I Learned

Metasploitable 2 is a great beginner machine: It exposes many different types of vulnerabilities, allowing practice in web, system, and service exploitation.

Enumeration matters: With so many open ports, learning how to prioritize targets was a valuable skill.

Default configurations are dangerous: Many real-world breaches happen because of weak or unchanged defaults.

Privilege escalation is about understanding the system: Misconfigurations and outdated software are often the key.

Safe practice environments are essential: This machine is perfect for experimentation without risk.

Conclusion

Metasploitable 2 helped me solidify my foundational penetration testing skills. It’s not a realistic machine like those found on CTF platforms, but it’s perfect for learning the basics, recognizing common vulnerabilities, and getting comfortable with the workflow of enumeration → exploitation → escalation.

Now that I've completed it, I’m ready to move onto more challenging labs and CTFs.

If you’re starting your cybersecurity journey, this machine is an excellent early practice target!
