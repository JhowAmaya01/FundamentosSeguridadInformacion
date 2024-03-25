## Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ea41c400c3c7b4a63406e5e607d362ab/shark1.pcapng).
## Solución
para encontrar la solución a este reto se siguieron los siguientes pasos
+ Primero se abrió el archivo en wireShark
+ Después se le dio clic derecho y se pudo en la opción de seguir paquetes TCP
+ Después cambiamos las secuencias y en cada uno vamos analizando el contenido
+ Después en la secuencia número 5 observamos lo siguiente: 
```
GET / HTTP/1.1

Host: 18.222.37.134

Connection: keep-alive

Cache-Control: max-age=0

Upgrade-Insecure-Requests: 1

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9

Accept-Encoding: gzip, deflate

Accept-Language: en-US,en;q=0.9

  

HTTP/1.1 200 OK

Date: Mon, 10 Aug 2020 01:51:45 GMT

Server: Apache/2.4.29 (Ubuntu)

Last-Modified: Fri, 07 Aug 2020 00:45:02 GMT

ETag: "2f-5ac3eea4fcf01"

Accept-Ranges: bytes

Content-Length: 47

Keep-Alive: timeout=5, max=100

Connection: Keep-Alive

Content-Type: text/html

  

Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
```
+ Al final se puede apreciar que hay un texto con un formato muy similar a las banderas que uno esta buscando, por lo que esté lo pasamos a un decodificador de rot13 y como resultado nos da lo siguiente: `The flag is picoCTF{p33kab00_1_s33_u_deadbeef}`
## Notas adicionales

## Referencias
