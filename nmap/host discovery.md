to check the system is on or off 

```bash
nmap -sn <target>
```

## test with ICMP protocol 
ICMP - Internet Control Message Protocol 
first the system send the ICMP echo request (type - 8) if the system is on then it will respond with ICMP echo replay (type - 0)

```bash
ping <target> -c <count>
```

