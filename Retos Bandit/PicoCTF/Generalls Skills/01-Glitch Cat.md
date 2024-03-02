## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 52682`
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ nc saturn.picoctf.net 52682
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
```
## Notas adicionales

+ La primera parte de la bandera es `picoCTF{gl17ch_m3_n07_` y los siguientes 9 caracteres son caracteres ASCII
+ Por lo que la bandera es la siguiente `picoCTF{gl17ch_m3_n07_bda68f75}`

## Referencias