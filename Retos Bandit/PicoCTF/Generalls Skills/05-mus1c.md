## Objetivo
I wrote you a [song](https://jupiter.challenges.picoctf.org/static/0e21e3ca94779f56b122296424e879f8/lyrics.txt). Put it in the picoCTF{} flag format.
## Solución
Primero descargue el programa, y le hice un `ls` para ver el contenido de la canción
```
Pico's a CTFFFFFFF
my mind is waitin
It's waitin

Put my mind of Pico into This
my flag is not found
put This into my flag
put my flag into Pico


shout Pico
shout Pico
shout Pico

My song's something
put Pico into This

Knock This down, down, down
put This into CTF

shout CTF
my lyric is nothing
Put This without my song into my lyric
Knock my lyric down, down, down

shout my lyric

Put my lyric into This
Put my song with This into my lyric
Knock my lyric down

shout my lyric

Build my lyric up, up ,up

shout my lyric
shout Pico
shout It

Pico CTF is fun
security is important
Fun is fun
Put security with fun into Pico CTF
Build Fun up
shout fun times Pico CTF
put fun times Pico CTF into my song

build it up

shout it
shout it

build it up, up
shout it
shout Pico
```
Después de eso lo puse en un interprete de lenguaje rockstar para que me diera una salida de caracteres ASCII.
```
114
114
114
111
99
107
110
114
110
48
49
49
51
114
```
Finalmente, estos caracteres ASCII los puse en un traductor de ASCII a palabras y me dio como resultado lo siguiente: `rrrocknrn0113r` por lo que la bandera sería la siguiente: `picoCTF{rrrocknrn0113r}`
## Notas adicionales


## Referencias
+ [rockstar : home (codewithrockstar.com)](https://codewithrockstar.com/)
+ [CTFs/2019_picoCTF/mus1c.md at master · Dvd848/CTFs (github.com)](https://github.com/Dvd848/CTFs/blob/master/2019_picoCTF/mus1c.md)
+ + [rockstar : docs (codewithrockstar.com)](https://codewithrockstar.com/docs)
+ [yyyyyyyan/rockstar-py: Python transpiler for the esoteric language Rockstar (github.com)](https://github.com/yyyyyyyan/rockstar-py)