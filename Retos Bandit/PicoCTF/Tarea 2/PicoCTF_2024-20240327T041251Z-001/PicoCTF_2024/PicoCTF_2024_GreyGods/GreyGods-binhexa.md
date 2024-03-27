## Player: GreyGods
## Goal

How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 62817`
## Solution

```bash
nc titan.picoctf.net 62817

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01010110
Binary Number 2: 10010001


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00010000
Correct!

Question 2/6:
Operation 2: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0011000010110110
Correct!

Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11100111
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01001000
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10101100
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11010111
Correct!

Enter the results of the last operation in hexadecimal: b7
Incorrect answer!

Enter the results of the last operation in hexadecimal: b 7

Incorrect input. Provide the right input!

Enter the results of the last operation in hexadecimal: 3131303130313131
Incorrect answer!

Enter the results of the last operation in hexadecimal: 3131303130313131
Incorrect answer!

Enter the results of the last operation in hexadecimal: D7

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}
````

## Notes

## References