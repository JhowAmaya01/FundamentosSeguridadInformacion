## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cat values
Decrypt my super sick RSA:
c: 62324783949134119159408816513334912534343517300880137691662780895409992760262021
n: 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
e: 65537
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ python3
Python 3.11.8 (main, Feb  7 2024, 21:52:08) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> p = 1899107986527483535344517113948531328331
>>> q = 674357869540600933870145899564746495319033
>>> n = p * q
>>> tn = (p -1) * (q - 1)
>>> e = 65537
>>> c = 62324783949134119159408816513334912534343517300880137691662780895409992760262021
>>> d = pow(e, -1, tn)
>>> m = pow(c, d, n)
>>> bytes.fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_05012767}'
>>>
```
## Notas adicionales

## Referencias