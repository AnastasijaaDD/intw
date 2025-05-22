Using nslookup in windows command prompt for a basic lookup I got the following results:


Server:  UnKnown\
Address:  192.168.0.1

Non-authoritative answer:\
beyondmachines.net      internet address = 3.164.85.66\
beyondmachines.net      internet address = 3.164.85.78\
beyondmachines.net      internet address = 3.164.85.40\
beyondmachines.net      internet address = 3.164.85.110\
beyondmachines.net      nameserver = ns-496.awsdns-62.com\
beyondmachines.net      nameserver = ns-543.awsdns-03.net\
beyondmachines.net      nameserver = ns-2019.awsdns-60.co.uk\
beyondmachines.net      nameserver = ns-1025.awsdns-00.org\
beyondmachines.net\
        primary name server = ns-543.awsdns-03.net\
        responsible mail addr = awsdns-hostmaster.amazon.com\
        serial  = 1\
        refresh = 7200 (2 hours)\
        retry   = 900 (15 mins)\
        expire  = 1209600 (14 days)\
        default TTL = 86400 (1 day)\
beyondmachines.net      MX preference = 5, mail exchanger = alt1.aspmx.l.google.com\
beyondmachines.net      MX preference = 1, mail exchanger = aspmx.l.google.com\
beyondmachines.net      MX preference = 10, mail exchanger = alt4.aspmx.l.google.com\
beyondmachines.net      MX preference = 10, mail exchanger = alt3.aspmx.l.google.com\
beyondmachines.net      MX preference = 5, mail exchanger = alt2.aspmx.l.google.com\
beyondmachines.net      text =

        "v=spf1 include:_spf.google.com ~all"\
beyondmachines.net      ??? unknown type 99 ???\

beyondmachines.net      nameserver = ns-496.awsdns-62.com\
beyondmachines.net      nameserver = ns-543.awsdns-03.net\
beyondmachines.net      nameserver = ns-2019.awsdns-60.co.uk\
beyondmachines.net      nameserver = ns-1025.awsdns-00.org\

Using subfinder, and then the "subfinder -d https://beyondmachines.net/" command in command prompt, I found the following subdomains, and with the ping command I checked if they are active\
used ssllabs to check for security and hosting checker for where it is hosted.
damascian.beyondmachines.net ---inactive\
challenge.beyondmachines.net  ---active, secure (A), hosted by:  Fastly, Inc, San Francisco, US\
yieldcat.beyondmachines.net ---- active, secure (A), hosted by: Render, San Francisco, US\
old.beyondmachines.net  --active, not trusted (T), hosted by: Automattic, Inc, San Francisco, US\
www.beyondmachines.net  -- active, secure (A), hosted by: Amazon.com, Inc, Ashburn, US\
ako.beyondmachines.net  --inactive\
rendertest.beyondmachines.net --inactive\
yieldhog.beyondmachines.net  --inactive\
damascian-online.beyondmachines.net  --inactive\
testalb.beyondmachines.net --inactive\
status.beyondmachines.net  --inactive\
clarity.beyondmachines.net  --inactive\
trust.beyondmachines.net  --active, secure(A+), hosted by: Cloudflare, Inc., Toronto, Canada\
[INF] Found 13 subdomains for beyondmachines.net in 22 seconds 466 milliseconds\



104.28.97.142 - - [06/May/2025:08:14:16 +0000] "GET /assets/js/script.js HTTP/1.1" 200 24689 "https://companyxyz.com/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:08:27:35 +0000] "GET /robots.txt HTTP/1.1" 404 452 "-" "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)"


45.33.49.201 - - [06/May/2025:08:27:42 +0000] "GET /.git/HEAD HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:08:44:08 +0000] "GET /.env HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:08:49:12 +0000] "GET /config.php HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:08:51:32 +0000] "GET /wp-login.php HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:09:12:27 +0000] "GET /phpmyadmin HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:09:13:05 +0000] "GET /backup HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:09:14:58 +0000] "GET /admin/login.php HTTP/1.1" 200 3452 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


121.18.83.75 - - [06/May/2025:09:23:42 +0000] "GET /products/search?q=phone%27%20OR%20%271%27%3D%271 HTTP/1.1" 500 1243 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:09:31:18 +0000] "GET /products/search?q=phone%27%3B%20DROP%20TABLE%20users%3B%20-- HTTP/1.1" 500 1243 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


45.33.49.201 - - [06/May/2025:10:02:05 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:02:08 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:02:11 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:02:14 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:02:17 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:02:20 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:13:42 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:13:45 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:13:48 +0000] "POST /admin/login.php HTTP/1.1" 302 0 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:32:15 +0000] "GET /admin/users.php HTTP/1.1" 200 12567 "https://companyxyz.com/admin/dashboard.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:37:22 +0000] "GET /admin/settings.php HTTP/1.1" 200 8754 "https://companyxyz.com/admin/users.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


198.51.100.73 - - [06/May/2025:10:42:16 +0000] "GET /blog/comment?id=15&text=<script>alert('XSS')</script> HTTP/1.1" 400 1253 "https://companyxyz.com/blog/article/15" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:123.0) Gecko/20100101 Firefox/123.0"


45.33.49.201 - - [06/May/2025:10:45:44 +0000] "GET /admin/backup.php HTTP/1.1" 200 4321 "https://companyxyz.com/admin/settings.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:47:02 +0000] "POST /admin/backup.php HTTP/1.1" 200 1289 "https://companyxyz.com/admin/backup.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:10:48:15 +0000] "GET /admin/backups/backup_06052025.zip HTTP/1.1" 200 1542783 "https://companyxyz.com/admin/backup.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


216.58.212.110 - - [06/May/2025:11:01:47 +0000] "GET /api/products HTTP/1.1" 200 47834 "-" "PostmanRuntime/7.32.3"


216.58.212.110 - - [06/May/2025:11:02:34 +0000] "GET /api/products/45892 HTTP/1.1" 200 1243 "-" "PostmanRuntime/7.32.3"


216.58.212.110 - - [06/May/2025:11:03:58 +0000] "GET /api/users HTTP/1.1" 403 321 "-" "PostmanRuntime/7.32.3"


121.18.83.75 - - [06/May/2025:11:42:33 +0000] "GET /download.php?file=../../../etc/passwd HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


45.33.49.201 - - [06/May/2025:11:56:12 +0000] "GET /uploads/shell.php HTTP/1.1" 200 18 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:11:56:48 +0000] "POST /uploads/shell.php HTTP/1.1" 200 4267 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:11:57:23 +0000] "POST /uploads/shell.php HTTP/1.1" 200 2198 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:11:58:05 +0000] "POST /uploads/shell.php HTTP/1.1" 200 43287 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


198.51.100.73 - - [06/May/2025:12:02:51 +0000] "GET /search?q=<img src="x" onerror="alert('XSS')"> HTTP/1.1" 400 1253 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:123.0) Gecko/20100101 Firefox/123.0"


216.58.212.110 - - [06/May/2025:12:15:37 +0000] "POST /api/orders HTTP/1.1" 401 341 "-" "PostmanRuntime/7.32.3"


216.58.212.110 - - [06/May/2025:12:16:12 +0000] "POST /api/orders HTTP/1.1" 201 982 "-" "PostmanRuntime/7.32.3"


121.18.83.75 - - [06/May/2025:12:34:27 +0000] "GET /api/products/42?callback=<script>alert(1)</script> HTTP/1.1" 400 1253 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:12:51:19 +0000] "POST /api/subscribe HTTP/1.1" 400 352 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:12:52:08 +0000] "POST /api/subscribe HTTP/1.1" 201 142 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


45.33.49.201 - - [06/May/2025:13:01:34 +0000] "POST /uploads/shell.php HTTP/1.1" 200 1854 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:13:17:20 +0000] "GET /admin/login.php HTTP/1.1" 200 3452 "https://companyxyz.com/admin/dashboard.php" "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0"


45.33.49.201 - - [06/May/2025:14:22:17 +0000] "GET /uploads/shell.php HTTP/1.1" 200 18 "-" "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:14:22:45 +0000] "POST /uploads/shell.php HTTP/1.1" 200 3542 "-" "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML


203.0.113.42 - - [06/May/2025:14:43:27 +0000] "POST /products/search HTTP/1.1" 200 10456 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:14:44:05 +0000] "POST /api/subscribe HTTP/1.1" 201 142 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:14:45:32 +0000] "POST /api/inventory HTTP/1.1" 403 321 "-" "python-requests/2.31.0"


45.33.49.201 - - [06/May/2025:15:02:14 +0000] "POST /uploads/shell.php HTTP/1.1" 200 18543 "-" "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML


121.18.83.75 - - [06/May/2025:15:13:45 +0000] "GET /cgi-bin/status?command=ls%20-la HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:15:14:26 +0000] "GET /cgi-bin/status?command=;cat%20/etc/passwd HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


216.58.212.110 - - [06/May/2025:15:37:28 +0000] "GET /api/products?limit=50&offset=100 HTTP/1.1" 200 68453 "-" "PostmanRuntime/7.32.3"


45.33.49.201 - - [06/May/2025:15:42:36 +0000] "POST /uploads/shell.php HTTP/1.1" 200 4387 "-" "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML


121.18.83.75 - - [06/May/2025:16:10:27 +0000] "GET /products/search?q=monitor%3Cscript%3Ealert(document.cookie)%3C/script%3E HTTP/1.1" 400 1253 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


45.33.49.201 - - [06/May/2025:16:23:05 +0000] "GET /uploads HTTP/1.1" 403 752 "-" "Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)"


45.33.49.201 - - [06/May/2025:16:23:18 +0000] "GET /uploads/ HTTP/1.1" 403 752 "-" "Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)"


45.33.49.201 - - [06/May/2025:16:23:32 +0000] "GET /uploads/shell.php HTTP/1.1" 200 18 "-" "Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)"


45.33.49.201 - - [06/May/2025:16:54:21 +0000] "POST /uploads/shell.php HTTP/1.1" 200 8765 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML


203.0.113.42 - - [06/May/2025:17:13:28 +0000] "GET /robots.txt HTTP/1.1" 200 452 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:17:13:45 +0000] "GET /sitemap.xml HTTP/1.1" 200 24536 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:17:15:22 +0000] "GET /api/products HTTP/1.1" 200 47834 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:17:17:13 +0000] "GET /api/categories HTTP/1.1" 200 2843 "-" "python-requests/2.31.0"


203.0.113.42 - - [06/May/2025:17:19:27 +0000] "GET /api/products?category=electronics HTTP/1.1" 200 32456 "-" "python-requests/2.31.0"


121.18.83.75 - - [06/May/2025:17:32:47 +0000] "GET /api/user/1/profile HTTP/1.1" 403 321 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:17:33:21 +0000] "GET /api/user/2/profile HTTP/1.1" 403 321 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


198.51.100.73 - - [06/May/2025:17:47:23 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:123.0) Gecko/20100101 Firefox/123.0"


45.33.49.201 - - [06/May/2025:17:53:18 +0000] "GET /uploads/shell.php HTTP/1.1" 200 18 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; Trident/7.0; rv:11.0) like Gecko"


45.33.49.201 - - [06/May/2025:17:53:35 +0000] "POST /uploads/shell.php HTTP/1.1" 200 6532 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; Trident/7.0; rv:11.0) like Gecko"


45.33.49.201 - - [06/May/2025:18:12:47 +0000] "POST /uploads/shell.php HTTP/1.1" 200 87654 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; Trident/7.0; rv:11.0) like Gecko"


45.33.49.201 - - [06/May/2025:18:51:43 +0000] "POST /uploads/shell.php HTTP/1.1" 200 12543 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; Trident/7.0; rv:11.0) like Gecko"


45.33.49.201 - - [06/May/2025:18:57:26 +0000] "GET /admin/login.php HTTP/1.1" 200 3452 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


121.18.83.75 - - [06/May/2025:19:03:18 +0000] "GET /api/status HTTP/1.1" 200 542 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:19:04:27 +0000] "GET /api/debug HTTP/1.1" 404 452 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


121.18.83.75 - - [06/May/2025:19:05:32 +0000] "GET /api/info HTTP/1.1" 200 1784 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML


45.33.49.201 - - [06/May/2025:19:12:04 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:12:07 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:12:10 +0000] "POST /admin/login.php HTTP/1.1" 401 752 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:12:13 +0000] "POST /admin/login.php HTTP/1.1" 302 0 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:12:14 +0000] "GET /admin/dashboard.php HTTP/1.1" 200 15867 "-" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:23:46 +0000] "GET /admin/users.php HTTP/1.1" 200 12567 "https://companyxyz.com/admin/dashboard.php" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:25:12 +0000] "GET /admin/user-edit.php?id=1 HTTP/1.1" 200 9823 "https://companyxyz.com/admin/users.php" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:27:34 +0000] "POST /admin/user-edit.php HTTP/1.1" 302 0 "https://companyxyz.com/admin/user-edit.php?id=1" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML


45.33.49.201 - - [06/May/2025:19:27:35 +0000] "GET /admin/users.php HTTP/1.1" 200 12567 "https://companyxyz.com/admin/user-edit.php?id=1" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML

Correctly Identified Threats
1. Sensitive File Probing

    Requests to:

        /.git/HEAD, /.env, /config.php, /wp-login.php, /phpmyadmin, /backup

    Assessment: Reconnaissance activity probing for exposed sensitive files.

2. SQL Injection Attempts

    Examples:

        /products/search?q=phone' OR '1'='1

        /products/search?q=phone'; DROP TABLE users; --

    Assessment: Confirmed SQL injection attempts (resulted in 500 errors).

3. XSS (Cross-Site Scripting) Attacks

    Examples:

        /search?q=<img src="x" onerror="alert('XSS')">

        /api/products/42?callback=<script>alert(1)</script>

        /products/search?q=monitor<script>alert(document.cookie)</script>

    Assessment: Clear attempts at injecting malicious scripts.

4. Command Injection & Directory Traversal

    Examples:

        /download.php?file=../../../etc/passwd

        /cgi-bin/status?command=;cat /etc/passwd

    Assessment: Attempts to execute commands or access restricted files.

5. Brute Force Login Attempts

    Repeated POST /admin/login.php requests (401 → 302) from 45.33.49.201.

    Assessment: Likely brute-force attack.

6. Web Shell Upload & Execution

    Multiple POST /uploads/shell.php and GET /uploads/shell.php requests.

    Assessment: Critical risk—attacker uploaded and executed a shell.

7. Unauthorized API Access Attempts

    Requests to /api/users, /api/user/1/profile, etc. (returning 403).

    Assessment: Probing for unauthorized data access.

Missed Attacks (False Negatives)
1. Successful Admin Dashboard Access After Brute-Force

    GET /admin/dashboard.php after multiple failed logins.

    Impact: Brute-force attack succeeded—critical security breach.

2. Data Exfiltration

    GET /admin/backups/backup_06052025.zip (1.5MB file downloaded).

    Impact: Sensitive data likely stolen.

3. Suspicious Backup Actions

    POST /admin/backup.php followed by GET /admin/backups/....

    Impact: Attacker may have generated a backup for exfiltration.

4. Automated Shell Access via Nmap

    GET /uploads/shell.php with Nmap Scripting Engine User-Agent.

    Impact: Automated exploitation attempt.

Possible False Positives
1. Static File Access

    GET /assets/js/script.js

    Assessment: Likely benign (normal static file request).

2. Googlebot Impersonation

    GET /robots.txt from 45.33.49.201 (claimed to be Googlebot).

    Assessment: Could be malicious if IP is suspicious.

3. Failed API Subscription

    POST /api/subscribe (failed once, then succeeded).

    Assessment: Possibly user error—not necessarily malicious.


Immediate Actions

  Block attacker IPs:

  45.33.49.201 (confirmed attacker with web shell).

  121.18.83.75 (SQLi/XSS attempts).

  Remove malicious files:

  Delete /uploads/shell.php and audit uploads directory.

  Patch vulnerabilities:

  Sanitize inputs in /products/search and APIs.

  Restrict /admin/ to whitelisted IPs + enforce 2FA.
