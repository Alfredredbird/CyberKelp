# Pretext
Gobuster is a popular web hacking tool used for scanning websites for hidden directories and files. The tool is often substituted with [[Dirbuster]] or [[FFuF]].
# Directory Scan
Using [[Tools#Gobuster|Gobuster]] is quite straight forward especially when it comes to a directory scan. We specify the directory scan with `dir`, our wordlist with `-w`, `-t` for the threads and `-x` for the file extensions to try to find.
```Bash
gobuster dir -u http://10.145.163.27:8080 -w ~/THM/WORDLISTS/DirBuster-2007_directory-list-2.3-medium.txt -t 100 -x txt,json,php
```

# Scan Types
As shown above, we can use `dir` for a directory scan and we can also use other values for different scans.

| Command                                        | Description                  |
| ---------------------------------------------- | ---------------------------- |
| dir                                            | `Directory Scan`             |
| vhost                                          | `Virtual Host Enumeration`   |
| dns                                            | `DNS Subdomain Enumeration`  |
| fuzz                                           | `Fuzzing Mode`               |
| tftp                                           | `TFTP Enumeration`           |
| s3                                             | `AWS Bucket Enumeration`     |
| gcs                                            | `GCS Buckey Enumeration`     |
| help                                           | `Help Menu`                  |
| ---------------------------------------------- | ---------------------------- |

# Expected Output

```
alfredredbird@Ubuntu-Novo:~/CyberKelp/.obsidian$ gobuster dir -u https://example.com -w ~/THM/list-2.3-medium.txt -t 100 
===============================================================
Gobuster v3.8.2
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     https://example.com
[+] Method:                  GET
[+] Threads:                 100
[+] Wordlist:                /home/alfredredbird/THM/list-2.3-medium.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.8.2
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
aspx                 (Status: 403) [Size: 4572]
phrack46             (Status: 403) [Size: 4572]
phrack47             (Status: 403) [Size: 4572]
phrack49             (Status: 403) [Size: 4572]
1751                 (Status: 403) [Size: 4572]
40HEX-02             (Status: 403) [Size: 4572]
home-loan            (Status: 403) [Size: 4572]

```