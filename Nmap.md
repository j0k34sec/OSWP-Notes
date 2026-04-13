After scanning our target to discover open ports and services, we can run **NSE scripts** to further enumerate the target.

exmaple:
```bash
nmap -p80 --script=http-enum $IP
```
