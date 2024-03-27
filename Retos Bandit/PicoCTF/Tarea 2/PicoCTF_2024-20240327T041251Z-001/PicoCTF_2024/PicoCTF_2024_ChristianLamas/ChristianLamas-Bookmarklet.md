## Objetivo
Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:58528/), and find the flag!
## Solución
Hal ir a la pagina nos da un bookmarklets 
```
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓË¨ËÓ§Èí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    
```
Este lo agregamos y nos da la bandera 
picoCTF{p@g3_turn3r_e8b2d43b}
## Notas adicionales
[Bookmarklets](https://es.wikipedia.org/wiki/Bookmarklet) son marcadores del navegador que ejecutan JavaScript en lugar de abrir una página web. También se conocen como applets de marcadores, favlets o marcadores de JavaScript.
## Referencias
[¿Qué son los Bookmarklets? Cómo usar JavaScript para hacer un Bookmarklet en Chromium y Firefox (freecodecamp.org)](https://www.freecodecamp.org/espanol/news/que-son-los-bookmarklets/)
