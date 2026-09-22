nse stands for nmap scripting engine. 
### 1. default script scan  

```bash
nmap -sC -p21 <target>
```

`-sC` is the default script scan. 

the default path of script directory `/usr/share/nmap/scripts/`

### 2. scan based on path 
```bash
nmap -p21 --script '/usr/share/nmap/script/ftp-anon.nse' 192.168.1.4
```

```bash
nmap -p21 --script 'ftp-anon.nse' 192.168.1.4
```

```
nmap -p21 --script 'ftp-anon' 192.168.1.4
```

```bash
nmap -p<ports> --script '<script1>,<script2>,...<scriptn>' <target>
```