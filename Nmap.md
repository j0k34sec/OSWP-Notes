After scanning our target to discover open ports and services, we can run **NSE scripts** to further enumerate the target.

exmaple:
```bash
nmap -p80 --script=http-enum $IP
```

![[Pasted image 20260413131553.png]]

If you want to know a specific 