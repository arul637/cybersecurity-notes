## states
- open - the port is open 
- closed - the port is closed
- filtered - the firewall is blocking the request

port is a gateway to communicate with the host, it play the vital role in application so it is helpful to find the port state is open or closed

there are totally 65535 ports 
- well known ports - `0 - 1023 `
- registered ports - `1024 - 49151` 
- dynamic/private/Ephemeral ports - `49152 - 65535`

|Port|Protocol|Service|
|--:|---|---|
|20|TCP|FTP Data|
|21|TCP|FTP Control|
|22|TCP|SSH|
|23|TCP|Telnet|
|25|TCP|SMTP|
|53|TCP/UDP|DNS|
|67|UDP|DHCP Server|
|68|UDP|DHCP Client|
|69|UDP|TFTP|
|80|TCP|HTTP|
|110|TCP|POP3|
|123|UDP|NTP|
|143|TCP|IMAP|
|161|UDP|SNMP|
|162|UDP|SNMP Trap|
|443|TCP|HTTPS|
|445|TCP|SMB|
|514|UDP|Syslog|
|587|TCP|SMTP Submission|
|631|TCP/UDP|IPP|
|993|TCP|IMAPS|
|995|TCP|POP3S|

|  Port | Service              |
| ----: | -------------------- |
|  1433 | Microsoft SQL Server |
|  1521 | Oracle Database      |
|  2049 | NFS                  |
|  3306 | MySQL                |
|  3389 | RDP                  |
|  5432 | PostgreSQL           |
|  5900 | VNC                  |
|  6379 | Redis                |
|  8080 | HTTP alternative     |
|  8443 | HTTPS alternative    |
| 27017 | MongoDB              |
|  5678 | n8n                  |

### 1. targeting single port
selecting the single port to find it is open or closed 

```bash
nmap -p<port> <target>
```

there is no space between `-p` and `port`

### 2. targeting multiple ports 
```bash
nmap -p21,22,23 192.168.1.4
```

### 3. targeting the range of ports
selecting the range from start to end, includes starts and end range

```bash
nmap -p100-1000 192.168.1.4
```

finding the open ports in between 100 to 1000 on host 192.168.1.4 

### 4. full port scan
scanning all ports.

```bash
nmap -p- 192.168.1.4
```

```bash
nmap -p1-65535 192.168.1.4
```

