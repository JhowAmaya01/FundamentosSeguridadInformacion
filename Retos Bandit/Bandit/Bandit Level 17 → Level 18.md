## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**
## Datos de acceso al nivel
bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
## Solución
```
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
## Notas adicionales
+ El comando head sirve para ver las primeras 10 líneas de un archivo

## Referencias
+ Ayuda del comando diff