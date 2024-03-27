## Objetivo
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)

## Solución
``` bash
aers-picoctf@webshell:~/CollaborativeDevelopment$ ls
challenge.zip
aers-picoctf@webshell:~/CollaborativeDevelopment$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
  inflating: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/77/
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
   creating: drop-in/.git/objects/6c/
 extracting: drop-in/.git/objects/6c/e09adec311b859780caf89d993c58e34b53fa6  
   creating: drop-in/.git/objects/6e/
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
   creating: drop-in/.git/objects/74/
 extracting: drop-in/.git/objects/74/ae5215b93a82ddf3dd37df3d4c6b5aff0a93ed  
   creating: drop-in/.git/objects/7a/
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
   creating: drop-in/.git/objects/d1/
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/b4/
 extracting: drop-in/.git/objects/b4/612c914d8461d1b1a50652cc303b76813ee142  
 extracting: drop-in/.git/objects/b4/5df8ce6725e05ed8f45745793f91c26f6529dc  
   creating: drop-in/.git/objects/59/
 extracting: drop-in/.git/objects/59/d9bf3f55055654fda549be87499374805f28e3  
   creating: drop-in/.git/objects/5c/
 extracting: drop-in/.git/objects/5c/6d493ac583a95117d3a70eb5b10d9d76991c48  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py         
  aers-picoctf@webshell:~/CollaborativeDevelopment$ cd drop-in
  aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git branch -a
  
aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ python3 flag.py
Printing the flag...
picoCTF{t3@mw0rk_aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git part-2ut feature/p
Switched to branch 'feature/part-2'
aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ python3 flag.py
Printing the flag...
m@k3s_th3_dr3@m_aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ 
aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
aers-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ python3 flag.py
Printing the flag...
w0rk_4c24302f}

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}

```

## Notas adicionales
Este conjunto de comandos permite revisar las diferentes ramas en el repositorio git y ejecutar el script en cada una de ellas para obtener diferentes partes de la bandera.