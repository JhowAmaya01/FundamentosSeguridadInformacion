## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
dolls.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ file dolls.jpg
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ file dolls.jpg
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
base_images  dolls.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cd base_images/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images]
└─$ ls
2_c.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images]
└─$ unzip 2_c.jpg
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images]
└─$ ls
2_c.jpg  base_images

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images]
└─$ cd base_images/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images]
└─$ unzip 2_c.jpg
unzip:  cannot find or open 2_c.jpg, 2_c.jpg.zip or 2_c.jpg.ZIP.

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images]
└─$ unzip 3_c.jpg
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images]
└─$ unzip 4_c.jpg
unzip:  cannot find or open 4_c.jpg, 4_c.jpg.zip or 4_c.jpg.ZIP.

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images]
└─$ ls
3_c.jpg  base_images

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images]
└─$ cd base_images/

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images/base_images]
└─$ unzip 4_c.jpg
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/base_images/base_images/base_images]
└─$ cat flag.txt
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}
```
## Notas adicionales

## Referencias
