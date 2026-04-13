After scanning our target to discover open ports and services, we can run **NSE scripts** to further enumerate the target.

exmaple:
```bash
nmap -p80 --script=http-enum $IP
```

![[Pasted image 20260413131553.png]]


So sometimes in some  directory  supports only some specific `HTTP Method`  LIKE `POST`, `DELETE`, `PUT` etc. in that case we can enumerate which http method is supported in that specific directory we can use this script.

```bash
nmap -p80 --script=http-methods --script-args http-methods.url-path='/wp-includes/' $IP
```
