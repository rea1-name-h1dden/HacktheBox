```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 --script="banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_nmap.txt" -oX "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/xml/tcp_80_http_nmap.xml" 10.10.11.166
```

[/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_nmap.txt](file:///home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_nmap.txt):

```
# Nmap 7.92 scan initiated Sat Aug 13 07:23:26 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_nmap.txt -oX /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/xml/tcp_80_http_nmap.xml 10.10.11.166
Nmap scan report for 10.10.11.166
Host is up, received user-set (0.065s latency).
Scanned at 2022-08-13 07:23:30 EDT for 268s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON  VERSION
80/tcp open  http    syn-ack nginx 1.14.2
|_http-chrono: Request times for /; avg: 341.13ms; min: 207.91ms; max: 710.98ms
| http-fileupload-exploiter: 
|   
|_    Couldn't find a file-type field.
|_http-server-header: nginx/1.14.2
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://use.fontawesome.com:443/releases/v6.1.0/js/all.js
|   https://cdn.jsdelivr.net:443/npm/bootstrap15.1.3/dist/js/bootstrap.bundle.min.js
|_  https://cdn.startbootstrap.com:443/sb-forms-0.4.1.js
|_http-feed: Couldn't find any feeds.
| http-headers: 
|   Server: nginx/1.14.2
|   Date: Sat, 13 Aug 2022 11:23:45 GMT
|   Content-Type: text/html
|   Content-Length: 5480
|   Last-Modified: Wed, 23 Mar 2022 16:34:04 GMT
|   Connection: close
|   ETag: "623b4bfc-1568"
|   Accept-Ranges: bytes
|   
|_  (Request type: HEAD)
| http-vhosts: 
| 123 names had status 200
| vpn
| www
| ns1
| vm
|_internal
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.11.166
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 7717
|     Comment: 
|         /* rtl:end:remove */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 20
|     Comment: 
|         <!-- Background Video-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 32
|     Comment: 
|         <!-- To make this form functional, sign up at-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 12
|     Comment: 
|         <!-- Google fonts-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 43
|     Comment: 
|         <!-- Submit success message-->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 257
|     Comment: 
|         /* rtl:ignore */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 57
|     Comment: 
|         <!-- This is what your users will see when there is-->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 6118
|     Comment: 
|         /* rtl:options: {
|           "autoRename": true,
|           "stringMap":[ {
|             "name"    : "prev-next",
|             "search"  : "prev",
|             "replace" : "next"
|           } ]
|         } */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 36
|     Comment: 
|         <!-- Email address input-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 46
|     Comment: 
|         <!-- has successfully submitted-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 78
|     Comment: 
|         <!-- * *                               SB Forms JS                               * *-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 45
|     Comment: 
|         <!-- This is what your users will see when the form-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 58
|     Comment: 
|         <!-- an error submitting the form-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 22
|     Comment: 
|         <!-- Masthead-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 55
|     Comment: 
|         <!-- Submit error message-->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 2
|     Comment: 
|         /*!
|         * Start Bootstrap - Coming Soon v6.0.6 (https://startbootstrap.com/theme/coming-soon)
|         * Copyright 2013-2022 Start Bootstrap
|         * Licensed under MIT (https://github.com/StartBootstrap/startbootstrap-coming-soon/blob/master/LICENSE)
|         */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 33
|     Comment: 
|         <!-- https://startbootstrap.com/solution/contact-forms-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 77
|     Comment: 
|         <!-- * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 65
|     Comment: 
|         <!-- For more icon options, visit https://fontawesome.com/icons?d=gallery&p=2&s=brands-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 16
|     Comment: 
|         <!-- Core theme CSS (includes Bootstrap)-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 34
|     Comment: 
|         <!-- to get an API token!-->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 7711
|     Comment: 
|         /* rtl:begin:remove */
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 6042
|     Comment: 
|         /* rtl:end:ignore */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 79
|     Comment: 
|         <!-- * * Activate your form at https://startbootstrap.com/solution/contact-forms * *-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 28
|     Comment: 
|         <!-- * * * * * * * * * * * * * * *-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 64
|     Comment: 
|         <!-- Social Icons-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 29
|     Comment: 
|         <!-- * * SB Forms Contact Form * *-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 31
|     Comment: 
|         <!-- This form is pre-integrated with SB Forms.-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 44
|     Comment: 
|         <!---->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 441
|     Comment: 
|         /* rtl:raw:
|         [type="tel"],
|         [type="url"],
|         [type="email"],
|         [type="number"] {
|           direction: ltr;
|         }
|         */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 73
|     Comment: 
|         <!-- Bootstrap core JS-->
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 4792
|     Comment: 
|         /* rtl: var(--bs-breadcrumb-divider, "/") */
|     
|     Path: http://10.10.11.166:80/js/scripts.js
|     Line number: 6
|     Comment: 
|         
|         // This file is intentionally blank
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 7
|     Comment: 
|         /*!
|          * Bootstrap v5.1.3 (https://getbootstrap.com/)
|          * Copyright 2011-2021 The Bootstrap Authors
|          * Copyright 2011-2021 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/main/LICENSE)
|          */
|     
|     Path: http://10.10.11.166:80/css/styles.css
|     Line number: 6031
|     Comment: 
|         /* rtl:begin:ignore */
|     
|     Path: http://10.10.11.166:80/
|     Line number: 75
|     Comment: 
|         <!-- Core theme JS-->
|     
|     Path: http://10.10.11.166:80/
|     Line number: 10
|     Comment: 
|_        <!-- Font Awesome icons (free version)-->
|_http-date: Sat, 13 Aug 2022 11:23:42 GMT; 0s from local time.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-errors: Couldn't find any error pages.
| http-useragent-tester: 
|   Status for browser useragent: 200
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
|_http-title: Coming Soon - Start Bootstrap Theme
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-malware-host: Host appears to be clean
|_http-mobileversion-checker: No mobile version detected.
| http-vuln-cve2011-3192: 
|   VULNERABLE:
|   Apache byterange filter DoS
|     State: VULNERABLE
|     IDs:  CVE:CVE-2011-3192  BID:49303
|       The Apache web server is vulnerable to a denial of service attack when numerous
|       overlapping byte ranges are requested.
|     Disclosure date: 2011-08-19
|     References:
|       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-3192
|       https://www.tenable.com/plugins/nessus/55976
|       https://www.securityfocus.com/bid/49303
|_      https://seclists.org/fulldisclosure/2011/Aug/175
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-php-version: Logo query returned unknown hash e716b8bf5e0fdacb3997e7f14f599386
|_Credits query returned unknown hash e716b8bf5e0fdacb3997e7f14f599386
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /assets/
|       ico: 1
|     /assets/mp4/
|       mp4: 1
|     /css/
|       css: 1
|     /js/
|       js: 1
|   Longest directory structure:
|     Depth: 2
|     Dir: /assets/mp4/
|   Total files found (by extension):
|_    Other: 1; css: 1; ico: 1; js: 1; mp4: 1
|_http-config-backup: ERROR: Script execution failed (use -d to debug)
|_http-favicon: Unknown favicon MD5: 556F31ACD686989B1AFCF382C05846AA
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-csrf: Couldn't find any CSRF vulnerabilities.
| http-methods: 
|_  Supported Methods: GET HEAD

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 13 07:27:59 2022 -- 1 IP address (1 host up) scanned in 272.91 seconds

```