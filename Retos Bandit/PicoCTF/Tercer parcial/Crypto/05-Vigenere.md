## Objetivo
Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/159/cipher.txt) using this key "CYLAB".
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/vigeniere]
└─$ cat cipher.txt
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_f85729e7}
```
Usando un decodificador online de vigenere y la clave obtuvimos la bandera la cual es la siguiente:
`picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}`
## Notas adicionales

## Referencias
+ [Vigenere Cipher - Online Decoder, Encoder, Solver, Translator (dcode.fr)](https://www.dcode.fr/vigenere-cipher 