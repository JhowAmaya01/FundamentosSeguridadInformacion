## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ ls
Addadshashanammu  Addadshashanammu.zip  static

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ cd

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[~]
└─$ ls

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[~]
└─$ cd /mnt/c/retospicoCTF

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ ls
Addadshashanammu  Addadshashanammu.zip  static

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ cd Addadshashanammu

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu]
└─$ ls
Almurbalarammi

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu]
└─$ cd Almurbalarammi

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi]
└─$ ls
Ashalmimilkala

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi]
└─$ cd Ashalmimilkala/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ ls
Assurnabitashpi

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ cd Assurnabitashpi/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└─$ cd Maelkashishi/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ cd Onnissiralis/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$  cd Ularradallaku/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ strings fang-of-haynekhtnamet | grep picoCTF
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}

```
## Notas adicionales
 + El comando `unzip` sirve para extraer un archivo que esta comprimido
 + Cuando en una carpeta se encuentra almacenado un único archivo el tabulador completa su nombre automaticamente
## Referencias