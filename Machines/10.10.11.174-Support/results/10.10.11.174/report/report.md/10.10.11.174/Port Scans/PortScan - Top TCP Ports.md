```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -sC --version-all -A --osscan-guess -oN "/home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/_quick_tcp_nmap.txt" -oX "/home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/xml/_quick_tcp_nmap.xml" 10.10.11.174
```

[/home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/_quick_tcp_nmap.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/_quick_tcp_nmap.txt):

```
# Nmap 7.93 scan initiated Wed Nov 23 09:19:53 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -sC --version-all -A --osscan-guess -oN /home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/_quick_tcp_nmap.txt -oX /home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/xml/_quick_tcp_nmap.xml 10.10.11.174
Nmap scan report for 10.10.11.174
Host is up, received user-set (0.026s latency).
Scanned at 2022-11-23 09:19:53 AEDT for 88s
Not shown: 989 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON  VERSION
53/tcp   open  domain        syn-ack Simple DNS Plus
88/tcp   open  kerberos-sec  syn-ack Microsoft Windows Kerberos (server time: 2022-11-22 22:20:01Z)
135/tcp  open  msrpc         syn-ack Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: support.htb0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack
464/tcp  open  kpasswd5?     syn-ack
593/tcp  open  ncacn_http    syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack
3268/tcp open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: support.htb0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped    syn-ack
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: 0s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 23794/tcp): CLEAN (Timeout)
|   Check 2 (port 19493/tcp): CLEAN (Timeout)
|   Check 3 (port 45724/udp): CLEAN (Timeout)
|   Check 4 (port 11620/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2022-11-22T22:20:44
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Nov 23 09:21:21 2022 -- 1 IP address (1 host up) scanned in 88.81 seconds

```