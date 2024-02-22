## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución
```
bandit20@bandit:~$ nc -lnvp 8080 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 4150578
bandit20@bandit:~$ Listening on 0.0.0.0 8080

bandit20@bandit:~$ ./suconnect 8080
Connection received on 127.0.0.1 46052
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```
## Notas adicionales
Para resolver este reto pudimos utilizar el comando tmux que se explica a continuación o bien utilizar la terminal en segundo plano.
+ tmux para entrar a una terminal "virtual" dentro de la terminal
+ ctrl + b " sirve para hacer dos ventanas en una terminal
+ ctrl + b space sirve para hacer dos ventanas en una terminal para hacer la division vertical/horizontal
+ ctrl + b % sirve para hacer dos ventanas en una terminal para division vertical
+ ctrl + flecha arriba/abajo para pasar a otra ventana cuando estan en division horizontal
+ ctrl + flecha derecha/izquierda para pasar a otra ventana cuando estan en division vertical
* 
## Referencias
+ Ayuda del comando nc