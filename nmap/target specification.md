### 1. scan with multiple hosts
separating the hosts with space
```bash
nmap 192.168.1.1 192.168.1.4 
```

### 2. scan with a file
a file which contain the full host list 
```bash
nmap -iL ips.txt
```
 
the `ips.txt` which contain host in list format 

