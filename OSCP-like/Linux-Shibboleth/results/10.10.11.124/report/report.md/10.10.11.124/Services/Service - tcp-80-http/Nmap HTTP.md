```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 --script="banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN "/home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/tcp_80_http_nmap.txt" -oX "/home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/xml/tcp_80_http_nmap.xml" 10.10.11.124
```

[/home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/tcp_80_http_nmap.txt](file:///home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/tcp_80_http_nmap.txt):

```
# Nmap 7.92 scan initiated Thu Nov  3 16:50:59 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/tcp_80_http_nmap.txt -oX /home/parallels/HacktheBox/OSCP-like/Linux-Shibboleth/results/10.10.11.124/scans/tcp80/xml/tcp_80_http_nmap.xml 10.10.11.124
Nmap scan report for shibboleth.htb (10.10.11.124)
Host is up, received user-set (0.053s latency).
Scanned at 2022-11-03 16:51:00 AEDT for 26s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON  VERSION
80/tcp open  http    syn-ack Apache httpd 2.4.41
|_http-malware-host: Host appears to be clean
|_http-exif-spider: ERROR: Script execution failed (use -d to debug)
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=shibboleth.htb
|   Found the following error pages: 
|   
|   Error Code: 404
|_  	http://shibboleth.htb:80/blog-singe.html
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-chrono: Request times for /; avg: 294.69ms; min: 258.37ms; max: 337.12ms
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=shibboleth.htb
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://shibboleth.htb:80/
|     Form id: 
|     Form action: forms/contact.php
|     
|     Path: http://shibboleth.htb:80/
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/blog.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/blog.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/index.html
|     Form id: 
|     Form action: forms/contact.php
|     
|     Path: http://shibboleth.htb:80/index.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/portfolio-details.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Form id: 
|     Form action: 
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Form id: 
|_    Form action: 
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-headers: 
|   Date: Thu, 03 Nov 2022 05:51:06 GMT
|   Server: Apache/2.4.41 (Ubuntu)
|   Last-Modified: Tue, 27 Apr 2021 15:38:05 GMT
|   ETag: "e852-5c0f60c60a3c3"
|   Accept-Ranges: bytes
|   Content-Length: 59474
|   Vary: Accept-Encoding
|   Connection: close
|   Content-Type: text/html
|   
|_  (Request type: HEAD)
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-config-backup: ERROR: Script execution failed (use -d to debug)
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; html: 1
|     /assets/img/
|       png: 5
|     /assets/img/clients/
|       png: 3
|     /assets/img/portfolio/
|       jpg: 3
|     /assets/img/team/
|       jpg: 1
|     /assets/js/
|       js: 1
|     /assets/vendor/isotope-layout/
|       js: 1
|     /assets/vendor/php-email-form/
|       js: 1
|     /assets/vendor/purecounter/
|       js: 1
|     /assets/vendor/swiper/
|       js: 1
|     /forms/
|       php: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /assets/img/portfolio/
|   Total files found (by extension):
|_    Other: 1; html: 1; jpg: 4; js: 5; php: 1; png: 8
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=shibboleth.htb
|     
|     Path: http://shibboleth.htb:80/assets/vendor/remixicon/remixicon.css
|     Line number: 1
|     Comment: 
|         /*
|         * Remix Icon v2.5.0
|         * https://remixicon.com
|         * https://github.com/Remix-Design/RemixIcon
|         *
|         * Copyright RemixIcon.com
|         * Released under the Apache License Version 2.0
|         *
|         * Date: 2020-05-23
|         */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 333
|     Comment: 
|         <!-- End Tab 1 Content -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 361
|     Comment: 
|         <!-- End Tab 3 Content -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 183
|     Comment: 
|         <!-- ======= Counts Section ======= -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 234
|     Comment: 
|         <!-- ======= Features Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 320
|     Comment: 
|         <!-- End blog entries list -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 16
|     Comment: 
|         <!-- Google Fonts -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 40
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/vendor/php-email-form/validate.js
|     Line number: 1
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 318
|     Comment: 
|         <!-- End blog comments -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 81
|     Comment: 
|         <!-- End Header -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 274
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 318
|     Comment: 
|         <!-- Tab Content -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 40
|     Comment: 
|         <!-- ======= Header ======= -->
|     
|     Path: http://shibboleth.htb:80/portfolio-details.html
|     Line number: 98
|     Comment: 
|         <!-- ======= Portfolio Details Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog.html
|     Line number: 98
|     Comment: 
|         <!-- ======= Blog Section ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/vendor/swiper/swiper-bundle.min.js
|     Line number: 1
|     Comment: 
|         /**
|          * Swiper 6.5.0
|          * Most modern mobile touch slider and framework with hardware accelerated transitions
|          * https://swiperjs.com
|          *
|          * Copyright 2014-2021 Vladimir Kharlampidi
|          *
|          * Released under the MIT License
|          *
|          * Released on: March 5, 2021
|          */
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 119
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 612
|     Comment: 
|         <!-- F.A.Q List 1-->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1059
|     Comment: 
|         <!-- ======= Clients Section ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 110
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 201
|     Comment: 
|         
|         
|         */
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 22
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 84
|     Comment: 
|         <!-- ======= Hero Section ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 10
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/vendor/remixicon/remixicon.css
|     Line number: 14
|     Comment: 
|         /* IE6-IE8 */
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 511
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 658
|     Comment: 
|         <!-- F.A.Q List 2-->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1217
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 94
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog.html
|     Line number: 318
|     Comment: 
|         <!-- End Blog Section -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 494
|     Comment: 
|         <!-- End Footer -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 195
|     Comment: 
|         <!-- End blog author bio -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 141
|     Comment: 
|         <!-- ======= Values Section ======= -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 965
|     Comment: 
|         <!-- ======= Team Section ======= -->
|     
|     Path: http://shibboleth.htb:80/portfolio-details.html
|     Line number: 146
|     Comment: 
|         <!-- End Portfolio Details Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1215
|     Comment: 
|         <!-- End Contact Section -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 498
|     Comment: 
|         <!-- Vendor JS Files -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 230
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 397
|     Comment: 
|         <!-- End sidebar -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 27
|     Comment: 
|         <!-- Template Main CSS File -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 963
|     Comment: 
|         <!-- End Testimonials Section -->
|     
|     Path: http://shibboleth.htb:80/assets/vendor/isotope-layout/isotope.pkgd.min.js
|     Line number: 1
|     Comment: 
|         /*!
|          * Isotope PACKAGED v3.0.6
|          *
|          * Licensed GPLv3 for open source use
|          * or Isotope Commercial License for commercial use
|          *
|          * https://isotope.metafizzy.co
|          * Copyright 2010-2018 Metafizzy
|          */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 373
|     Comment: 
|         <!-- Feature Icons -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 514
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 347
|     Comment: 
|         <!-- End Tab 2 Content -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1
|     Comment: 
|         
|         
|         
|         
|         
|         */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1129
|     Comment: 
|         <!-- End Recent Blog Posts Section -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 158
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 78
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 34
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 305
|     Comment: 
|         <!-- Tabs -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 110
|     Comment: 
|         <!-- ======= About Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 97
|     Comment: 
|         <!-- End Breadcrumbs -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 421
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 156
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 30
|     Comment: 
|         
|         
|         
|         
|         
|           ======================================================== -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1013
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 378
|     Comment: 
|         <!-- End sidebar recent posts-->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 399
|     Comment: 
|         <!-- End blog sidebar -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 198
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 213
|     Comment: 
|         <!-- End comment #1 -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 488
|     Comment: 
|         <!-- You can delete the links only if you purchased the pro version. -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 490
|     Comment: 
|         <!-- Purchase the pro version with working PHP/AJAX contact form: https://bootstrapmade.com/flexstart-bootstrap-startup-template/ -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 443
|     Comment: 
|         <!-- End Features Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 371
|     Comment: 
|         <!-- End Feature Tabs -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 232
|     Comment: 
|         <!-- End Counts Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1131
|     Comment: 
|         <!-- ======= Contact Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 487
|     Comment: 
|         <!-- All the links in the footer should remain intact. -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1044
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 8
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 194
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 395
|     Comment: 
|         <!-- End sidebar tags-->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 709
|     Comment: 
|         <!-- ======= Portfolio Section ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 599
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1084
|     Comment: 
|         <!-- End Clients Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 445
|     Comment: 
|         <!-- ======= Services Section ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 246
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 33
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 439
|     Comment: 
|         <!-- End Feature Icons -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 319
|     Comment: 
|         
|         
|         */
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1369
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 404
|     Comment: 
|         <!-- End Blog Single Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 316
|     Comment: 
|         <!-- End Tabs -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 408
|     Comment: 
|         <!-- ======= Footer ======= -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1686
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1086
|     Comment: 
|         <!-- ======= Recent Blog Posts Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 259
|     Comment: 
|         <!-- End comment #2-->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 257
|     Comment: 
|         <!-- End comment reply #1-->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 600
|     Comment: 
|         <!-- ======= F.A.Q Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 507
|     Comment: 
|         <!-- Template Main JS File -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 2192
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 891
|     Comment: 
|         <!-- End testimonial item -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 181
|     Comment: 
|         <!-- End Values Section -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 288
|     Comment: 
|         <!-- End comment #4 -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 862
|     Comment: 
|         <!-- End Portfolio Section -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 489
|     Comment: 
|         <!-- Licensing information: https://bootstrapmade.com/license/ -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1560
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 78
|     Comment: 
|         <!-- .navbar -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 72
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1496
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1467
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 165
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 344
|     Comment: 
|         <!-- End sidebar categories-->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 223
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/assets/vendor/remixicon/remixicon.css
|     Line number: 18
|     Comment: 
|         /* iOS 4.1- */
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 1282
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 914
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 139
|     Comment: 
|         <!-- End About Section -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 180
|     Comment: 
|         <!-- End blog entry -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 636
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 123
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 707
|     Comment: 
|         <!-- End F.A.Q Section -->
|     
|     Path: http://shibboleth.htb:80/assets/vendor/remixicon/remixicon.css
|     Line number: 13
|     Comment: 
|         /* IE9*/
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 60
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 85
|     Comment: 
|         <!-- ======= Breadcrumbs ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 99
|     Comment: 
|         <!-- ======= Blog Single Section ======= -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 107
|     Comment: 
|         <!-- End Hero -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 864
|     Comment: 
|         <!-- ======= Testimonials Section ======= -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 517
|     Comment: 
|         <!-- ======= Pricing Section ======= -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 332
|     Comment: 
|         <!-- End sidebar search formn-->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 1057
|     Comment: 
|         <!-- End Team Section -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 515
|     Comment: 
|         <!-- End Services Section -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 567
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 406
|     Comment: 
|         <!-- End #main -->
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 274
|     Comment: 
|         <!-- End comment #3 -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 147
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 19
|     Comment: 
|         <!-- Vendor CSS Files -->
|     
|     Path: http://shibboleth.htb:80/assets/js/main.js
|     Line number: 129
|     Comment: 
|         
|         
|            */
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 12
|     Comment: 
|         <!-- Favicons -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 298
|     Comment: 
|         <!-- / row -->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 598
|     Comment: 
|         <!-- End Pricing Section -->
|     
|     Path: http://shibboleth.htb:80/assets/css/style.css
|     Line number: 761
|     Comment: 
|         
|         
|         --------------------------------------------------------------*/
|     
|     Path: http://shibboleth.htb:80/blog-single.html
|     Line number: 255
|     Comment: 
|         <!-- End comment reply #2-->
|     
|     Path: http://shibboleth.htb:80/index.html
|     Line number: 300
|     Comment: 
|         <!-- Feature Tabs -->
|     
|     Path: http://shibboleth.htb:80/assets/vendor/remixicon/remixicon.css
|     Line number: 17
|     Comment: 
|_        /* chrome, firefox, opera, Safari, Android, iOS 4.2+*/
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
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
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-mobileversion-checker: No mobile version detected.
|_http-title: FlexStart Bootstrap Template - Index
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-date: Thu, 03 Nov 2022 05:51:08 GMT; 0s from local time.
| http-enum: 
|   
|_  /forms/: Potentially interesting directory w/ listing on 'apache/2.4.41 (ubuntu)'
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-favicon: Unknown favicon MD5: FED84E16B6CCFE88EE7FFAAE5DFEFD34
| http-vhosts: 
|_128 names had status 302
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
| http-php-version: Logo query returned unknown hash 74a846063ca515ec5e236fa702cfd4b3
|_Credits query returned unknown hash 74a846063ca515ec5e236fa702cfd4b3
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-grep: 
|   (2) http://shibboleth.htb:80/: 
|     (2) email: 
|       + info@example.com
|_      + contact@example.com
|_http-feed: Couldn't find any feeds.

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Nov  3 16:51:26 2022 -- 1 IP address (1 host up) scanned in 26.47 seconds

```
