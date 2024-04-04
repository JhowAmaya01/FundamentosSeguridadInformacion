## Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext).
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ file ciphertext
ciphertext: ASCII text, with no line terminators

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cat ciphertext
picoCTF{gvswwmrkxlivyfmgsrhnrisegl}


Metiendo esto a un decodificador cesar y moviendolo 22 posiciones como reultado nos da el siguiente
picoCTF{crossingtherubicondjneoach}

```
## Notas adicionales

## Referencias
+ [Caesar Cipher - Privacy Canada](https://privacycanada.net/classical-encryption/caesar-cipher/)