```bash
whatweb --color=never --no-errors -a 3 -v http://10.10.10.48:80 2>&1
```

[/home/parallels/HacktheBox/OSCP-like/Linux-Mirai/results/10.10.10.48/scans/tcp80/tcp_80_http_whatweb.txt](file:///home/parallels/HacktheBox/OSCP-like/Linux-Mirai/results/10.10.10.48/scans/tcp80/tcp_80_http_whatweb.txt):

```
WhatWeb report for http://10.10.10.48:80
Status    : 404 Not Found
Title     : <None>
IP        : 10.10.10.48
Country   : RESERVED, ZZ

Summary   : HTTPServer[lighttpd/1.4.35], lighttpd[1.4.35], UncommonHeaders[x-pi-hole]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : lighttpd/1.4.35 (from server string)

[ UncommonHeaders ]
	Uncommon HTTP server headers. The blacklist includes all
	the standard headers and many non standard but common ones.
	Interesting but fairly common headers should have their own
	plugins, eg. x-powered-by, server and x-aspnet-version.
	Info about headers can be found at www.http-stats.com

	String       : x-pi-hole (from headers)

[ lighttpd ]
	Lightweight open-source web server.

	Version      : 1.4.35
	Website     : http://www.lighttpd.net/

HTTP Headers:
	HTTP/1.1 404 Not Found
	X-Pi-hole: A black hole for Internet advertisements.
	Content-type: text/html; charset=UTF-8
	Content-Length: 0
	Connection: close
	Date: Sun, 18 Sep 2022 05:13:33 GMT
	Server: lighttpd/1.4.35



```