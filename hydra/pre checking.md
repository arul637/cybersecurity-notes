checking the attacking port is open or closed use nmap tool for this 

[[target specification]]
[[port specifications]]
[[scanning techniques]]

```bash
administrator@administrator:~$ nmap -p21 -sV 192.168.1.3
Starting Nmap 7.98 ( https://nmap.org ) at 2026-09-22 10:10 +0530
Nmap scan report for Unknown_08:00:27:5c:9e:14 (192.168.1.3)
Host is up (0.00043s latency).

PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 2.3.4
Service Info: OS: Unix

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 0.26 seconds
administrator@administrator:~$
```

```bash
administrator@administrator:~$ sudo nmap -p3306 -sS -sV 192.168.1.3 

[sudo: authenticate] Password:      
Starting Nmap 7.98 ( https://nmap.org ) at 2026-09-22 10:49 +0530
Nmap scan report for Unknown_08:00:27:5c:9e:14 (192.168.1.3)
Host is up (0.00021s latency).

PORT     STATE SERVICE VERSION
3306/tcp open  mysql   MySQL 5.0.51a-3ubuntu5
MAC Address: 08:00:27:5C:9E:14 (Oracle VirtualBox virtual NIC)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 0.26 seconds
```

