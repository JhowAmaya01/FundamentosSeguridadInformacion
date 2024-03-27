## Player: GreyGods 
## Goal
Know of little and big endian?
[Source](https://artifacts.picoctf.net/c_titan/79/flag.c)
## Hints
+ You might want to check the ASCII table to first find the hexadecimal representation of characters before finding the endianness.
+ Read more about how endianness [here](https://levelup.gitconnected.com/little-endian-and-big-endian-74ab6441b2a7)
## Solution
### Primary terminal
```bash
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $wget https://artifacts.picoctf.net/c_titan/79/flag.c
--2024-03-16 01:21:49--  https://artifacts.picoctf.net/c_titan/79/flag.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3666 (3.6K) [application/octet-stream]
Saving to: ‘flag.c’

flag.c              100%[===================>]   3.58K  --.-KB/s    in 0s      

2024-03-16 01:21:50 (29.9 MB/s) - ‘flag.c’ saved [3666/3666]

┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $ls
flag.c
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $nano flag.c 
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $nc titan.picoctf.net 56615
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: wkgzm
Enter the Little Endian representation: 6d7a676b77
Correct Little Endian representation!
Enter the Big Endian representation: 776b677a6d
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_d58517b6}

````

### Secundary terminal
```bash
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $nano findLittleBigEndian.py
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $cat f
findLittleBigEndian.py  flag.c                  
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $cat findLittleBigEndian.py 
def ascii_to_hex(text_string):
  """
  Converts an ASCII string to its hexadecimal representation.

  Args:
    text_string: The ASCII string to convert.

  Returns:
    A bytearray containing the hexadecimal representation of the string.
  """
  return bytearray(text_string.encode('ascii'))

def change_endianness(hex_data, order):
  """
  Swaps the byte order within a hexadecimal bytearray.

  Args:
    hex_data: A bytearray containing hexadecimal data.
    order: The desired byte order ("little" or "big").

  Returns:
    A bytearray with the byte order changed.
  """
  if order == "little":
    return hex_data[::-1]
  elif order == "big":
    return hex_data
  else:
    raise ValueError("Invalid byte order: " + order)

def main():
  # Ask the user to enter the string
  text_string = input("Enter an ASCII string: ")

  # Convert to hexadecimal
  hex_data = ascii_to_hex(text_string)

  # Convert to Little Endian
  little_endian = change_endianness(hex_data, "little")

  # Convert to Big Endian
  big_endian = change_endianness(hex_data, "big")

  # Display results
  print("ASCII String:", text_string)
  print("Little Endian:", "".join("%02x" % b for b in little_endian))
  print("Big Endian:", "".join("%02x" % b for b in big_endian))

if __name__ == "__main__":
  main()
┌─[parrot@parrot]─[~/picoCTF2024/endianness]
└──╼ $python3 findLittleBigEndian.py 
Enter an ASCII string: wkgzm
ASCII String: wkgzm
Little Endian: 6d7a676b77
Big Endian: 776b677a6d
````

## Notes

## References

