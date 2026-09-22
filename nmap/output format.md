### 1. txt output 
save the nmap output in txt file
```bash
nmap -p<port> -sV -sT <target> -oN <filename>
```

#### example
```bash
nmap -p21 -sV -sS 192.168.1.4 -oN ftp.txt --stat-every 5s
```

the nmap results saved in `ftp.txt`  , here `--stats-every` represent display the output in every 5s 

### 2. XML output 
save the nmap results in XML file, later it is converted into html using `xsltproc` 
```
nmap -p<ports> <options> <target> -oX <filename>
```

#### example
```bash
nmap -p21 -sV -sS 192.168.1.4 -oX ftp.xml
```

#### converting the xml into html
```
xsltproc ftp.xml -o ftp.html
```