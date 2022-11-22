```bash
whatweb --color=never --no-errors -a 3 -v http://10.10.11.182:80 2>&1
```

[/home/parallels/HacktheBox/Machines/10.10.11.182-Photobomb/results/10.10.11.182/scans/tcp80/tcp_80_http_whatweb.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.182-Photobomb/results/10.10.11.182/scans/tcp80/tcp_80_http_whatweb.txt):

```
WhatWeb report for http://10.10.11.182:80
Status    : 302 Found
Title     : 302 Found
IP        : 10.10.11.182
Country   : RESERVED, ZZ

Summary   : HTTPServer[Ubuntu Linux][nginx/1.18.0 (Ubuntu)], nginx[1.18.0], RedirectLocation[http://photobomb.htb/]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : nginx/1.18.0 (Ubuntu) (from server string)

[ RedirectLocation ]
	HTTP Server string location. used with http-status 301 and
	302

	String       : http://photobomb.htb/ (from location)

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 302 Moved Temporarily
	Server: nginx/1.18.0 (Ubuntu)
	Date: Tue, 22 Nov 2022 05:39:41 GMT
	Content-Type: text/html
	Content-Length: 154
	Connection: close
	Location: http://photobomb.htb/



```