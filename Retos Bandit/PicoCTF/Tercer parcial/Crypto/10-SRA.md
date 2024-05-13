## Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...Connect to the program on our server: `nc saturn.picoctf.net 55924`Download the program: [chal.py](https://artifacts.picoctf.net/c/299/chal.py)
## Solución
Hacemos un script en python para poder resolver el problema,
```
from sage.all import *

from pwn import *

from gmpy2 import is_prime

from string import ascii_letters, digits

from Crypto.Util.number import bytes_to_long, long_to_bytes, inverse

  

r = remote('saturn.picoctf.net', 54972)

  

def is_printable(text):

    alphabet = ascii_letters + digits

    for i in text:

        if i not in alphabet:

            return False

    return True

  

e = 65537

r.recvuntil(b'anger = ')

c = int(r.recvline().strip().decode())

r.recvuntil(b'envy = ')

d = int(r.recvline().strip().decode())

r.recvline()

print(c)

print(d)

  

K = divisors(d*e - 1)

print("Done")

  

list_prime = []

for k in K:

    pp = ((d*e - 1)//k) + 1

  

    if is_prime(pp) and int(pp).bit_length() == 128:

        list_prime.append(pp)

  

list_text = []

for p in list_prime:

    for q in list_prime:

        try:

            if inverse(e, (p - 1) * (q - 1)) == d:

                n = p*q

                list_text.append(long_to_bytes(int(pow(c, d, n))))

        except:

            pass

  
  

list_text = set(list_text)

  

for text in list_text:

    try:

        text = text.decode()

        if is_printable(text):

            print(text)

            r.recvuntil(b'> ')

            r.sendline(text.encode())

            print(r.recvline())

            print(r.recvline())

            print(r.recvline())

            break

    except:

        continue

r.close()
```
Una vez hecho esto ejecutamos el script y obtenemos la bandera:
```
jhow@DESKTOP-Q5FQ7BC:/mnt/c/retospicoCTF/SRA$ python3 SRA2.py
[+] Opening connection to saturn.picoctf.net on port 54972: Done
69124805715192363936881695008338535018371281756067743041264113662309778721501
58015136820005614427660974272570877611940548021782851377326315926969139165993
Done
TLnX5iPJ3zlT6ufm
b'TLnX5iPJ3zlT6ufm\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_3858bd66}\r\n'
[*] Closed connection to saturn.picoctf.net port 54972
```
## Notas adicionales

## Referencias
+ [PicoCTF2023_Writeup/files at master · Cyberguru1/PicoCTF2023_Writeup (github.com)](https://github.com/Cyberguru1/PicoCTF2023_Writeup/tree/master/files)