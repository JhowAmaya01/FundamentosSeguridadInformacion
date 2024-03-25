## Objetivo
Can you get the flag? Here's the [website](http://saturn.picoctf.net:55793/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solución
Para filtrar los phats tenemos que escribir `../../../../flag.txt` para que nos pueda mostrar la bandera, pues todos los txt viven en la ruta predeterminada, pero la bandera se encuentra en el directorio raíz.
`picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}`
## Notas adicionales

## Referencias
