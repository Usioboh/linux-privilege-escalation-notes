# Linux Privilege Escalation Notes

A hands-on documentation of privilege escalation 
techniques that were carried out in a controlled legal lab environment 
as part of my cybersecurity learning journey.

## What This Demonstrates

- Linux system enumeration
- SUID binary exploitation
- Kernel vulnerability research and exploitation
- Privilege escalation via misconfigurations
- Offensive security methodology
- Use of industry standard tools (Metasploit, searchsploit, LinPEAS, GTFOBins)

## Techniques Covered

| # | Techniques ...
| 01 | Kernel Exploits 
| 02 | Stored Passwords (Config Files)
| 03 | Stored Passwords (History)
| 04 | Weak File Permissions
| 05 | SSH Keys
| 06 | Sudo (Shell Escaping)
| 07 | Sudo (Abusing Intended Functionality
| 08 | LD_PRELOAD
| 09 | SUID (Shared Object Injection)
| 10 | SUID (Symlinks)
| 11 | SUID (Environment Variables)
| 12 | SUID (Environment Variables 2)
| 13 | Linux Capabilities
| 14 | Cron (Path)
| 15 | Cron (Wildcards)
| 16 | Cron (File Overwrite)
| 17 | NFS Root Squashing

## How To Review

Start with `01-kernel-exploits` and work through 
each folder in order. Each folder contains a write-up 
with the concept explained.

## Tools Used

- Kali Linux
- TryHackMe Labs
- Metasploit Framework
- Searchsploit
- LinPEAS
- GCC

## Safety / Scope

All activity was performed in legal, controlled lab 
environments specifically designed for security training.
No real systems were targeted at any point.

## About Me

Aspiring penetration tester working toward eJPT and PNPT 
certifications. Documenting my journey publicly to build 
a professional portfolio.
