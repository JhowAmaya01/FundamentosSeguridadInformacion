## Player: GreyGods
## Goal

Description
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?
Download the suspicious file here.
## Solution

```bash
┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $wget https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf
--2024-03-14 01:29:53--  https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf  100%[===================>]   3.28K  --.-KB/s    in 0s      

2024-03-14 01:29:54 (94.9 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]

┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $ls
flag2of2-final.pdf
┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $open flag2of2-final.pdf 
┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $open flag2of2-final.pdf 
┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $cp flag2of2-final.pdf flag2of2-final.png
┌─[parrot@parrot]─[~/picoCTF_2024/Polyglot]
└──╼ $open flag2of2-final.png 
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
````


## Notes

## References