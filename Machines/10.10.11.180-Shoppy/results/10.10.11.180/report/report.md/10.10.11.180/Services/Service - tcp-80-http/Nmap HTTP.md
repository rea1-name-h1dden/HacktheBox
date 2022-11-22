```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 --script="banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN "/home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/tcp_80_http_nmap.txt" -oX "/home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/xml/tcp_80_http_nmap.xml" 10.10.11.180
```

[/home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/tcp_80_http_nmap.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/tcp_80_http_nmap.txt):

```
# Nmap 7.93 scan initiated Tue Nov 22 11:22:08 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/tcp_80_http_nmap.txt -oX /home/parallels/HacktheBox/Machines/10.10.11.180-Shoppy/results/10.10.11.180/scans/tcp80/xml/tcp_80_http_nmap.xml 10.10.11.180
Nmap scan report for 10.10.11.180
Host is up, received user-set (0.026s latency).
Scanned at 2022-11-22 11:22:08 AEDT for 81s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON  VERSION
80/tcp open  http    syn-ack nginx 1.23.1
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-comments-displayer: Couldn't find any comments.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-chrono: ERROR: Script execution failed (use -d to debug)
| http-useragent-tester: 
|   Status for browser useragent: false
|   Redirected To: http://shoppy.htb
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     Python-urllib/2.5
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     HTTP::Lite
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-config-backup: ERROR: Script execution failed (use -d to debug)
|_http-passwd: ERROR: Script execution failed (use -d to debug)
|_http-feed: Couldn't find any feeds.
|_http-server-header: nginx/1.23.1
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-mobileversion-checker: No mobile version detected.
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-sitemap-generator: 
|   Directory structure:
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    
|_http-errors: Couldn't find any error pages.
| http-headers: 
|   Server: nginx/1.23.1
|   Date: Tue, 22 Nov 2022 00:22:19 GMT
|   Content-Type: text/html
|   Content-Length: 169
|   Connection: close
|   Location: http://shoppy.htb
|   
|_  (Request type: GET)
|_http-csrf: Couldn't find any CSRF vulnerabilities.
| http-vhosts: 
|_128 names had status 301
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-title: Did not follow redirect to http://shoppy.htb
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-date: Tue, 22 Nov 2022 00:22:16 GMT; -1s from local time.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-malware-host: Host appears to be clean

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Nov 22 11:23:29 2022 -- 1 IP address (1 host up) scanned in 81.44 seconds

```