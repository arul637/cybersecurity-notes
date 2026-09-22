needs 
- hash mode 
- attack type / attack mode 

hash mode:
	the number that represent the hash type or hash format weather it might be md5, or sha1 etc..,

attack type:
	how to perform the attack dictionary attack or bruteforce attack 

```
Built-in charsets
       ?l = abcdefghijklmnopqrstuvwxyz
       ?u = ABCDEFGHIJKLMNOPQRSTUVWXYZ
       ?d = 0123456789
       ?h = 0123456789abcdef
       ?H = 0123456789ABCDEF
       ?s =  !"#$%&'()*+,-./:;<=>?@[]^_`{|}~
       ?a = ?l?u?d?s
       ?b = 0x00 - 0xff
```

```
Attack mode
       0 = Straight
       1 = Combination
       3 = Brute-force
       6 = Hybrid Wordlist + Mask
       7 = Hybrid Mask + Wordlist

Hash types
       0 = MD5
       10 = md5($pass.$salt)
       20 = md5($salt.$pass)
       30 = md5(unicode($pass).$salt)
       40 = md5($salt.unicode($pass))
       50 = HMAC-MD5 (key = $pass)
       60 = HMAC-MD5 (key = $salt)
       100 = SHA1
       110 = sha1($pass.$salt)
       120 = sha1($salt.$pass)
       130 = sha1(unicode($pass).$salt)
       140 = sha1($salt.unicode($pass))
       150 = HMAC-SHA1 (key = $pass)
       160 = HMAC-SHA1 (key = $salt)
       200 = MySQL323
       300 = MySQL4.1/MySQL5
       400 = phpass, MD5(Wordpress), MD5(phpBB3), MD5(Joomla)
       500 = md5crypt, MD5(Unix), FreeBSD MD5, Cisco-IOS MD5
       900 = MD4
       1000 = NTLM
       1100 = Domain Cached Credentials (DCC), MS Cache
       1400 = SHA256
       1410 = sha256($pass.$salt)
       1420 = sha256($salt.$pass)
       1430 = sha256(unicode($pass).$salt)
       1431 = base64(sha256(unicode($pass)))
       1440 = sha256($salt.unicode($pass))
       1450 = HMAC-SHA256 (key = $pass)
       1460 = HMAC-SHA256 (key = $salt)
       1600 = md5apr1, MD5(APR), Apache MD5
       1700 = SHA512
       1710 = sha512($pass.$salt)
       1720 = sha512($salt.$pass)
       1730 = sha512(unicode($pass).$salt)
       1740 = sha512($salt.unicode($pass))
       1750 = HMAC-SHA512 (key = $pass)
       1760 = HMAC-SHA512 (key = $salt)
       1800 = SHA-512(Unix)
       2400 = Cisco-PIX MD5
       2410 = Cisco-ASA MD5
       2500 = WPA/WPA2
       2600 = Double MD5
       3200 = bcrypt, Blowfish(OpenBSD)
       3300 = MD5(Sun)
       3500 = md5(md5(md5($pass)))
       3610 = md5(md5($salt).$pass)
       3710 = md5($salt.md5($pass))
       3720 = md5($pass.md5($salt))
       3800 = md5($salt.$pass.$salt)
       3910 = md5(md5($pass).md5($salt))
       4010 = md5($salt.md5($salt.$pass))
       4110 = md5($salt.md5($pass.$salt))
       4210 = md5($username.0.$pass)
       4300 = md5(strtoupper(md5($pass)))
       4400 = md5(sha1($pass))
       4500 = Double SHA1
       4600 = sha1(sha1(sha1($pass)))
       4700 = sha1(md5($pass))
       4800 = MD5(Chap), iSCSI CHAP authentication
       4900 = sha1($salt.$pass.$salt)
       5000 = SHA-3(Keccak)
       5100 = Half MD5
       5200 = Password Safe SHA-256
       5300 = IKE-PSK MD5
       5400 = IKE-PSK SHA1
       5500 = NetNTLMv1-VANILLA / NetNTLMv1-ESS
       5600 = NetNTLMv2
       5700 = Cisco-IOS SHA256
       5800 = Android PIN
       6300 = AIX {smd5}
       6400 = AIX {ssha256}
       6500 = AIX {ssha512}
       6700 = AIX {ssha1}
       6900 = GOST, GOST R 34.11-94
       7000 = Fortigate (FortiOS)
       7100 = OS X v10.8+
       7200 = GRUB 2
              7300 = IPMI2 RAKP HMAC-SHA1
       7400 = sha256crypt, SHA256(Unix)
       7900 = Drupal7
       8400 = WBB3, Woltlab Burning Board 3
       8900 = scrypt
       9200 = Cisco $8$
       9300 = Cisco $9$
       9800 = Radmin2
       10000 = Django (PBKDF2-SHA256)
       10200 = Cram MD5
       10300 = SAP CODVN H (PWDSALTEDHASH) iSSHA-1
       11000 = PrestaShop
       11100 = PostgreSQL Challenge-Response Authentication (MD5)
       11200 = MySQL Challenge-Response Authentication (SHA1)
       11400 = SIP digest authentication (MD5)
       99999 = Plaintext

Specific hash type
       11 = Joomla < 2.5.18
       12 = PostgreSQL
       21 = osCommerce, xt:Commerce
       23 = Skype
       101 = nsldap, SHA-1(Base64), Netscape LDAP SHA
       111 = nsldaps, SSHA-1(Base64), Netscape LDAP SSHA
       112 = Oracle S: Type (Oracle 11+)
       121 = SMF > v1.1
       122 = OS X v10.4, v10.5, v10.6
       123 = EPi
       124 = Django (SHA-1)
       131 = MSSQL(2000)
       132 = MSSQL(2005)
       133 = PeopleSoft
       141 = EPiServer 6.x < v4
       1421 = hMailServer
       1441 = EPiServer 6.x > v4
       1711 = SSHA-512(Base64), LDAP {SSHA512}
       1722 = OS X v10.7
       1731 = MSSQL(2012 & 2014)
       2611 = vBulletin < v3.8.5
       2612 = PHPS
       2711 = vBulletin > v3.8.5
       2811 = IPB2+, MyBB1.2+
       3711 = Mediawiki B type
       3721 = WebEdition CMS
       7600 = Redmine Project Management Web App
```

### examples 

```
administrator@administrator:~$ echo 'hello'
hello
administrator@administrator:~$ echo -n 'hello'
helloadministrator@administrator:~$
```

while using `echo` we need to preserve the newline

```
administrator@administrator:~$ echo -n 'password123' | md5sum 
482c811da5d5b4bc6d497ffa98491e38  -
```

### 1. find the hash id 

need to identify the given hash format, for that we can use the hashid tool or hash-identifier tool

```bash
apt search hashid
sudo apt install hashid
```

```
administrator@administrator:~$ hashid 482c811da5d5b4bc6d497ffa98491e38 -m
Analyzing '482c811da5d5b4bc6d497ffa98491e38'
[+] MD2 
[+] MD5 [Hashcat Mode: 0]
[+] MD4 [Hashcat Mode: 900]
[+] Double MD5 [Hashcat Mode: 2600]
[+] LM [Hashcat Mode: 3000]
[+] RIPEMD-128 
[+] Haval-128 
[+] Tiger-128 
[+] Skein-256(128) 
[+] Skein-512(128) 
[+] Lotus Notes/Domino 5 [Hashcat Mode: 8600]
[+] Skype [Hashcat Mode: 23]
[+] Snefru-128 
[+] NTLM [Hashcat Mode: 1000]
[+] Domain Cached Credentials [Hashcat Mode: 1100]
[+] Domain Cached Credentials 2 [Hashcat Mode: 2100]
[+] DNSSEC(NSEC3) [Hashcat Mode: 8300]
[+] RAdmin v2.x [Hashcat Mode: 9900]
```

`-m` to display the mode for the hashcat format. 

```
administrator@administrator:~$ hashcat -m 0 -a 0 482c811da5d5b4bc6d497ffa98491e38 /opt/seclists/Passwords/Leaked-Databases/rockyou.txt
```

here `-m 0` represent `md5` 
`-a 0` dictionary attack 
hash and wordlist 

```bash
administrator@administrator:~$ echo -n 'password123' | sha256sum 
ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f  -
administrator@administrator:~$ hashid -m ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f 
Analyzing 'ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f'
[+] Snefru-256 
[+] SHA-256 [Hashcat Mode: 1400]
[+] RIPEMD-256 
[+] Haval-256 
[+] GOST R 34.11-94 [Hashcat Mode: 6900]
[+] GOST CryptoPro S-Box 
[+] SHA3-256 [Hashcat Mode: 5000]
[+] Skein-256 
[+] Skein-512(256) 
administrator@administrator:~$ 

```

```
administrator@administrator:~$ hashcat -m 1400 -a 0 ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f /opt/seclists/Passwords/Leaked-Databases/rockyou.txt
```

next example for bruteforce attack 

```bash
administrator@administrator:~$ echo -n '1234' | md5sum 
81dc9bdb52d04dc20036dbd8313ed055  -
administrator@administrator:~$ hashid 81dc9bdb52d04dc20036dbd8313ed055 -m 
Analyzing '81dc9bdb52d04dc20036dbd8313ed055'
[+] MD2 
[+] MD5 [Hashcat Mode: 0]
[+] MD4 [Hashcat Mode: 900]
[+] Double MD5 [Hashcat Mode: 2600]
[+] LM [Hashcat Mode: 3000]
[+] RIPEMD-128 
[+] Haval-128 
[+] Tiger-128 
[+] Skein-256(128) 
[+] Skein-512(128) 
[+] Lotus Notes/Domino 5 [Hashcat Mode: 8600]
[+] Skype [Hashcat Mode: 23]
[+] Snefru-128 
[+] NTLM [Hashcat Mode: 1000]
[+] Domain Cached Credentials [Hashcat Mode: 1100]
[+] Domain Cached Credentials 2 [Hashcat Mode: 2100]
[+] DNSSEC(NSEC3) [Hashcat Mode: 8300]
[+] RAdmin v2.x [Hashcat Mode: 9900]
administrator@administrator:~$ hashcat -m 0 -a 3 81dc9bdb52d04dc20036dbd8313ed055 ?d?d?d?d
```