## Player: GreyGods 
## Goal
Can you control your overflow?Download the binary [here](https://artifacts.picoctf.net/c_tethys/3/chall).Download the source [here](https://artifacts.picoctf.net/c_tethys/3/chall.c).
Additional details will be available after launching your challenge instance.
## Hints
How can you tell where safe_var starts?
## Solution

I was repeating the word pico in the buffer so that safe_var would equal pico and get the flag.

```bash
Heap State:
+-------------+----------------+
[*] Address   ->   Heap Data   
+-------------+----------------+
[*]   0x55927d46d2b0  ->   picopicopicopicopicopicopicopicopico
+-------------+----------------+
[*]   0x55927d46d2d0  ->   pico
+-------------+----------------+

1. Print Heap:          (print the current state of the heap)
2. Write to buffer:     (write to your own personal block of data on the heap)
3. Print safe_var:      (I'll even let you look at my variable on the heap, I'm confident it can't be modified)
4. Print Flag:          (Try to print the flag, good luck)
5. Exit

Enter your choice: 4

YOU WIN
picoCTF{starting_to_get_the_hang_c588b8a1}
````
## Notes

## References
