## Objetivo
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 42248`.
## Solución
Se hace un programa en python para poder resolver el problema:
```
from Crypto.Util.number import *

from pwn import *

from decimal import *

import re

  

getcontext().prec = 1000

  

conn = remote('mercury.picoctf.net', 42248)

raw_text = conn.recvuntil('Give me ciphertext to decrypt:').decode()

  

print(raw_text)

  

m = re.search(r"n: ([0-9]+)\ne: ([0-9]+)\nciphertext: ([0-9]+)", raw_text)

n = int(m[1])

e = int(m[2])

c = int(m[3])

  

to_decrypt = c * pow(2, e, n) % n

  

conn.send(str(to_decrypt) + '\r\n')

  

print("Sent:", to_decrypt)

  

result = conn.recvline().decode()

  

print(result)

  

m = re.search(r"([0-9]+)", result)

result = int(Decimal(m[1]) / 2)

  

print(hex(result))

print('Result:', long_to_bytes(result))

print(binascii.unhexlify(st))
```
Una vez que ejecutamos el programa desde consola obtenemos la bandera:
```
jhow@DESKTOP-Q5FQ7BC:/mnt/c/retospicoctf/NoPaddingNoProblem$ python3 Exploit.py
[+] Opening connection to mercury.picoctf.net on port 30048: Done
/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py:9: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  raw_text = conn.recvuntil('Give me ciphertext to decrypt:').decode()
Welcome to the Padding Oracle Challenge
This oracle will take anything you give it and decrypt using RSA. It will not accept the ciphertext with the secret message... Good Luck!


n: 160714573698210589838802608592399115727648233814552242916161147122784282441819132391997902068304827406395883934117097229699325732604546541313314531366283074779511786193334504181492597503152195652937160477749702490394999947579509842562383592913581093777017784107667132939894859845950392599945806786741669086571
e: 65537
ciphertext: 96366197065476516339877600020892065381316502152762254587836042937216326415576890970696568447970720256080730602540888970106206197467548917788990383276511637158011155001373420764294732962412679424525117826051564221795367189189342239445359881912396649959024703594122302163184723391662230851003289764625812471347


Give me ciphertext to decrypt:
/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py:20: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.send(str(to_decrypt) + '\r\n')
Sent: 66919842286707259472633740784016764178376961313359937303084187988757610627221608259834866055535580063015181650665020811666863837294525921244915434042988408675351248009418292558328806364208030976722755030958654090554301597643193066291318712091160325319314950232217673967903775327253284695920493749091913506895
 Here you go: 580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890769425795379846471930

0x7069636f4354467b6d347962335f54683073655f6d337335346733735f3472335f646966757272656e745f353035323632307d
Result: b'picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_5052620}'
Traceback (most recent call last):
  File "/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py", line 33, in <module>
    print(binascii.unhexlify(st))
NameError: name 'st' is not defined
[*] Closed connection to mercury.picoctf.net port 30048
jhow@DESKTOP-Q5FQ7BC:/mnt/c/retospicoctf/NoPaddingNoProblem$ python3 Exploit.py
[+] Opening connection to mercury.picoctf.net on port 42248: Done
/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py:9: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  raw_text = conn.recvuntil('Give me ciphertext to decrypt:').decode()
Welcome to the Padding Oracle Challenge
This oracle will take anything you give it and decrypt using RSA. It will not accept the ciphertext with the secret message... Good Luck!


n: 90156850044523242537397625013883507476959662614735464222554121355060252247012497332020161918918488905870639115380542490304772230812730274117107199722012073167948477437370169867893278613473484140994334067248056432286448385234200785876136737363079273915021795241090832076008799138291355873120944554156059030459
e: 65537
ciphertext: 46780014530824393227064838860374916555195594484729607766958584061434126233503146280194095255354842774618228807580524132336734875262728601531775759438626573983619068413233185684594253732680717868747205315989423079524067201713729829778967711189960240301503383903272572612941589568420902177774130914914056688338


Give me ciphertext to decrypt:
/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py:20: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.send(str(to_decrypt) + '\r\n')
Sent: 15976254374249908283387228925387751796732979847332748290542650149194196301946506444332887685548452898698137956949724952940707592070295344831137167610173909156285179883915910907462605170438625377788791115855052910065109273516833586741066081545862793955117735989410320329105096403819879090309155103914236860695
 Here you go: 580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890769716268793877259514

0x7069636f4354467b6d347962335f54683073655f6d337335346733735f3472335f646966757272656e745f373431363032327d
Result: b'picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_7416022}'
Traceback (most recent call last):
  File "/mnt/c/retospicoctf/NoPaddingNoProblem/Exploit.py", line 33, in <module>
    print(binascii.unhexlify(st))
NameError: name 'st' is not defined
[*] Closed connection to mercury.picoctf.net port 42248
```
## Notas adicionales

## Referencias
+ [No Padding, No Problem (90) | CTFs (zeyu2001.com)](https://ctf.zeyu2001.com/2021/picoctf/no-padding-no-problem-90)