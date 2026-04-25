
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
we can discover live parameters  form url endpoints

```bash
wfuzz -c FOR COLOR OUTPUT -z To SPECIFY THE INPUT SOUCE --hc TO FILTER OUT USING STATUS CODE http://target.xyz/index.php?FUZZ=data 
```

with the same way we can discover parameter values by changing in the target url `http://target.xyz/index.php?fpv=FUZZ`
## Fuzz `POST` data form a http request using WFUZZ 
basically we can also fuzz data from `POST` data from HTTP requests

```bash
wfuzz -c FOR COLOR OUTPUT -z To SPECIFY THE INPUT SOUCE --hc TO FILTER OUT USING STATUS CODE -d POST DATA HERE   --hh 6059 http://target.xyz/wp-login.php
```

using the `--hh 6059` you can ignore the responses which have 6059 line you can add other number after analyzing response before.
