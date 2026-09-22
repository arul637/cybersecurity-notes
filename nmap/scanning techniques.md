if the port is open we will get the response `ack`, if the port is closed then we will get response with `rst + ack`

### 1. full TCP scan 
full complete 3 way handshake will happen here to find the port is open 

```bash
nmap -p21 -sT 192.168.1.1
```

here specifying the port 21 to find this port open or close using full TCP connect scan 

### 2. stealth scan 
half-tcp handshake will happens here, the attacker send `syn` request to server, the server responds with `syn + ack` that's all we can determine if we get packet then the port is open 
if we get `rst` (reset) then the port is closed

```bash
nmap -p21 -sS 192.168.1.1
```

### 3. xmas scan 
sending the packets by turning on `psh, urg, fin` to the server, this is unwanted packet format, if the port is open then we wont get any replay, if the port is closed then we will get `rst`.

```bash
nmap -p21 -sX 192.168.1.1
```

### 4. version detection scan
grabbing the banner for the serve by sending various packets 

```bash
nmap -sV -p<ports> <target>
```

### 5. null scan
`-sN` sending the packet with no TCP flags, similarly to XMAS scan, if the port is open then no replay will come, if the port is closed then we will get `rst + ack`. 

### 6. fin scan 
`-sF` sending the packet with TCP fin flag, similarly to XMAS scan, if the port is open then no replay will come, if the port is closed then we will get `rst + ack`