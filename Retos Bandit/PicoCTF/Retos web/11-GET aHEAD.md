## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[~]
└─$ curl -I HEAD http://mercury.picoctf.net:21939/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
Content-type: text/html; charset=UTF-8
```
## Notas adicionales

## Referencias
+ [Métodos de petición HTTP - HTTP | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/HTTP/Methods)