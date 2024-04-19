## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
Primero mostramos lo que hay en archivo que descargamos
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cat message.txt
350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213
```
Después sacamos la lógica que tenemos que seguir para poder hacer un programa en python para que nos ayude a resolver el reto. Los números cuyo mod sea igual o mayor a 0 e igual o menor a 25 son letras mayúsculas, por lo que si vemos en una tabla ascii estos  caracteres comienzan en el número 65, por lo que podemos hacer es al modo que nos resultó sumar 65; para el caso en donde el mod sea igual o mayor a 26 e igual o menor a 35 son números, en la tabla ascii estos comienzan a partir del 48, por lo que al restar 48 - 26 nos da un resultado de 22, es decir, hay que sumar 22 al modo que nos salió para saber que digito es; y finalmente cuyos números cuyo mod sea igual a 36 se cambia por un guion bajo.
Una vez obtenida esta lógica procedemos a realizar un programa como el siguiente:
```
datos = open("message.txt").read().split()

  

flag = ""

c = ""

for n in datos:

    i = int(n) % 37

    if i >= 0 and i <= 25:

        c = chr(i + 65)

    elif i>= 26 and i<=35:

        c = chr(i +22)

    else:

        c = "_"

    flag  = flag + c

print(flag)
```
Al momento de ejecutar el programa nos da como resultado:
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ python3 Basic-mod1.py
R0UND_N_R0UND_ADD17EC2
```

## Notas adicionales

## Referencias