## Objetivo
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
challenge.zip  ciphertext  convert.py  drop-in  flag2of2-final.pdf

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ mv flag2of2-final.pdf flag2of2-final.png

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
challenge.zip  ciphertext  convert.py  drop-in  flag2of2-final.png
```
La primera parte de la bandera es `picoCTF{f1u3n7_` 
La segunda parte se encuentra al abrir el pdf que nos da la descarga.
`1n_pn9_&_pdf_7f9bccd1}`
Por lo que la bandera es 
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
## Notas adicionales

## Referencias
