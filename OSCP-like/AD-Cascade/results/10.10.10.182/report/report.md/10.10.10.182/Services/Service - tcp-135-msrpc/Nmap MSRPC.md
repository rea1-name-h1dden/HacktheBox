```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 135 --script="banner,msrpc-enum,rpc-grind,rpcinfo" -oN "/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/tcp_135_rpc_nmap.txt" -oX "/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/xml/tcp_135_rpc_nmap.xml" 10.10.10.182
```

[/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/tcp_135_rpc_nmap.txt](file:///home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/tcp_135_rpc_nmap.txt):

```
# Nmap 7.93 scan initiated Fri Nov 18 15:56:55 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 135 --script=banner,msrpc-enum,rpc-grind,rpcinfo -oN /home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/tcp_135_rpc_nmap.txt -oX /home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp135/xml/tcp_135_rpc_nmap.xml 10.10.10.182
Nmap scan report for 10.10.10.182
Host is up, received user-set (0.023s latency).
Scanned at 2022-11-18 15:57:02 AEDT for 21s

PORT    STATE SERVICE REASON  VERSION
135/tcp open  msrpc   syn-ack Microsoft Windows RPC
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Nov 18 15:57:23 2022 -- 1 IP address (1 host up) scanned in 28.72 seconds

```
