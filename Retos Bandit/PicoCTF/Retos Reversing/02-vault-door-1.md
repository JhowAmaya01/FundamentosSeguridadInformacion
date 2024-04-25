## Objetivo
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/VaultDoor1]
└─$ cat flag | sort | awk '{print($3)}'
'd'
'_'
't'
'H'
'3'
'3'
'_'
'c'
'H'
'4'
'r'
'4'
'c'
'T'
'3'
'r'
'5'
'5'
'_'
'6'
'd'
'a'
'f'
'4'
'c'
'r'
'4'
'm'
'b'
'l'
'3'

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/VaultDoor1]
└─$ cat flag | sort -n | awk '{print($3)}'
'd'
'3'
'5'
'c'
'r'
'4'
'm'
'b'
'l'
'3'
'_'
't'
'H'
'3'
'_'
'c'
'H'
'4'
'r'
'4'
'c'
'T'
'3'
'r'
'5'
'_'
'6'
'd'
'a'
'f'
'4'

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/VaultDoor1]
└─$ cat flag | sort -n | awk '{print($3)}' | tr -d "'" | tr  -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_6daf4
```
## Notas adicionales

## Referencias
+ [10 ejemplos útiles del comando Sort en Linux (itsfoss.com)](https://itsfoss.com/es/comando-sort-linux/)
+ [Uso del comando AWK en Linux y UNIX con ejemplos (geekland.eu)](https://geekland.eu/uso-del-comando-awk-en-linux-y-unix-con-ejemplos/)