## Objetivo
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
files.zip

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8
  inflating: files/satisfactory_books/23765.txt.utf-8
  inflating: files/satisfactory_books/16021.txt.utf-8
  inflating: files/13771.txt.utf-8
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
  inflating: files/adequate_books/more_books/1023.txt.utf-8
  inflating: files/adequate_books/46804-0.txt
  inflating: files/adequate_books/44578.txt.utf-8
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8
  inflating: files/acceptable_books/17880.txt.utf-8
  inflating: files/acceptable_books/17879.txt.utf-8
  inflating: files/14789.txt.utf-8

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
files  files.zip

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cd files

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/files]
└─$ ls
13771.txt.utf-8  14789.txt.utf-8  acceptable_books  adequate_books  satisfactory_books

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/files]
└─$ find -name uber-secret.txt
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/files]
└─$ cat adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}

```
## Notas adicionales

## Referencias
+ [Linux find | Cómo usar el comando find de Linux - IONOS MX](https://www.ionos.mx/digitalguide/servidores/configuracion/comando-linux-find/)