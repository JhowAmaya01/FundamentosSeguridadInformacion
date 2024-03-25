## Objetivo
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:64727/).
## Solución
Para localizar la bandera inspeccionamos el código fuente y observamos que existe una carpeta llamada secrets, entonces al siguiente URL: `http://saturn.picoctf.net:64727/`, le agregamos la extensión `secret/`, con esto nos manda a una pagina que contiene una imagen que dice que vamos por el lugar correcto, entonces, volvemos a analizar el código fuente de la página y este contiene una carpeta llamada hidden, entonces tomamos el link anterior `http://saturn.picoctf.net:64727/secret/` y le agregamos `hidden/` con esta nueva extensión nos manda a una pagina para iniciar sesión en alguna página, y volvemos a analizar su código fuente, dentro de este hay una nueva carpeta llamada superhidden, por lo que volvemos a tomar el URL anterior `http://saturn.picoctf.net:64727/secret/hidden/` y le agregamos `superhiden/` y este nos manda un mensaje que dice que finalmente lo encontramos pero no podemos verlo, por lo que por última vez analizamos el código fuente de la página y es ahí donde encontramos la bandera.
```
|   |   |
|---|---|
||<!DOCTYPE html>|
||<html>|
||<head>|
||<title></title>|
||<link rel="stylesheet" href="[mycss.css](http://saturn.picoctf.net:64727/secret/hidden/superhidden/mycss.css)" />|
||</head>|
|||
||<body>|
||<h1>Finally. You found me. But can you see me</h1>|
||<h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_790d2615}</h3>|
||</body>|
||</html>|
```
## Notas adicionales

## Referencias
