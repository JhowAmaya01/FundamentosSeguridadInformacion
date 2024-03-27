## Objetivo
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/3/enc_flag).
## Solución
Primero mostramos lo que contiene el archivo
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==
```
Despues de eso utilizamos cyberchef para decodificar de base64, y obtenemos  
`b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2kyMDRoa2o2fQ=='` y decodificamos nuevamente lo que esta entre comillas obteniendo `wpjvJAM{jhlzhy_k3jy9wa3k_i204hkj6}`. Después decodificamos con cifrado cesar 12 veces mas para obtener la bandera `picoCTF{caesar_d3cr9pt3d_b204adc6}` 

## Notas adicionales

## Referencias