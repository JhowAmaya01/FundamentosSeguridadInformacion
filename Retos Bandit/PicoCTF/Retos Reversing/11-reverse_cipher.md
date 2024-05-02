## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.
## Solución
Primero realizamos un análisis en Ghidra y observamos la función main, una vez que hemos decompilado el programa, en ella podemos observar lo siguiente:
```
  size_t sVar1;
  char local_58 [23];
  char local_41;
  int local_2c;
  FILE *local_28;
  FILE *local_20;
  uint local_14;
  int local_10;
  char local_9;
  
  local_20 = fopen("flag.txt","r");
  local_28 = fopen("rev_this","a");
  if (local_20 == (FILE *)0x0) {
    puts("No flag found, please make sure this is run on the server");
  }
  if (local_28 == (FILE *)0x0) {
    puts("please run this on the server");
  }
  sVar1 = fread(local_58,0x18,1,local_20);
  local_2c = (int)sVar1;
  if ((int)sVar1 < 1) {
                    /* WARNING: Subroutine does not return */
    exit(0);
  }
  for (local_10 = 0; local_10 < 8; local_10 = local_10 + 1) {
    local_9 = local_58[local_10];
    fputc((int)local_9,local_28);
  }
  for (local_14 = 8; (int)local_14 < 0x17; local_14 = local_14 + 1) {
    if ((local_14 & 1) == 0) {
      local_9 = local_58[(int)local_14] + '\x05';
    }
    else {
      local_9 = local_58[(int)local_14] + -2;
    }
    fputc((int)local_9,local_28);
  }
  local_9 = local_41;
  fputc((int)local_41,local_28);
  fclose(local_28);
  fclose(local_20);
  return;
```
Observamos que hay 2 ciclos for, uno que imprime la parte de la bandera que hace aparecer `picoCTF{}` y la otra parte la imprime cifrada en donde la posición del carácter si al hacer un and el resultado es 0 le suma 5 posiciones, pero si es un 1  le resta dos posiciones, por lo que para resolver este reto realizamos un scrip en python de la siguiente manera:
```
d = open('rev_this', 'r').read()

  

flag = ""

for j in range (8,len(d)-1):

    if j&1 == 0:

        flag += chr( ord(d[j]) - 5)

    else:

        flag += chr( ord(d[j]) + 2)

  

print(flag)
```

Al momento de correrlo en consola nos da como resultado el siguiente:
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/reverseCipher]
└─$ python3 exploit.py
r3v3rs312528e05
```
La cual es la parte faltante de la bandera
## Notas adicionales

## Referencias