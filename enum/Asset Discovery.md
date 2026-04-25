
# Gobuster

## subdomain enumeration using Gobuster  
along side with directory busting we can also enumerate subdomains (active enumeration) with gobuster Tool

```bash
gobuster dns -d test.xyz -w /path/to/wordlist.txt -t THREAD COUNT
```


# WFUZZ
## Directory Busting and File enumeration using WFUZZ
using this tool we can discover hidden files and directory from a website 

```bash
wfuzz -c FOR COLOR OUTPUT -z To SPECIFY THE INPUT SOUCE --hc TO FILTER OUT USING STATUS CODE target.xyz/FUZZ 
```

with this will only discover the files, btu fi we add a `/` afrer the fuzz like this `target.xyz/FUZZ/` it will start fuzzing directories

## Parameter Discover using wfuzz
