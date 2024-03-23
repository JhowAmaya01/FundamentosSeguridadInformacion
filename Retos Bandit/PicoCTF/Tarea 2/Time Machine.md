## Objetivo
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/68/challenge.zip)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/drop-in]
└─$ cat message.txt
This is what I was working on, but I'd need to look at my commit history to know why...
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/drop-in]
└─$ git status message.txt
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   message.txt

no changes added to commit (use "git add" and/or "git commit -a")

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/drop-in]
└─$ git log
commit 705ff639b7846418603a3272ab54536e01e3dc43 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:36 2024 +0000

    picoCTF{t1m3m@ch1n3_b476ca06}
```
## Notas adicionales

## Referencias
+ [El Control de Versiones con Git: Rastreando Cambios (swcarpentry.github.io)](https://swcarpentry.github.io/git-novice-es/04-changes.html)