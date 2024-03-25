## Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/195/network-dump.flag.pcap)
## Solución
 Primero se abrió el archivo en wireShark
+ Después se le dio clic derecho y se pudo en la opción de seguir paquetes TCP
+ Después, al abrir la ventana lo primero que se muestra es lo siguiente:
```
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ b 9 d 5 3 7 6 5 }
```
+ Ahora solo tenemos que quitar los espacios entre cada caracter para introducir la bandera.
`picoCTF{p4ck37_5h4rk_b9d53765}`
## Notas adicionales

## Referencias
