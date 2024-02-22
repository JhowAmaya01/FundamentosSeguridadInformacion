## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solución
```
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2024-02-22 01:45 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.07 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31046
CONNECTED(00000003)
80DBF0F7FF7F0000:error:0A0000F4:SSL routines:ossl_statem_client_read_transition:unexpected message:../ssl/statem/statem_clnt.c:398:
---
no peer certificate available
---
No client certificate CA names sent
---
SSL handshake has read 293 bytes and written 300 bytes
Verification: OK
---
New, (NONE), Cipher is (NONE)
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 0 (ok)
---
bandit16@bandit:~$ openssl s_client -connect localhost:31518
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:07 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:07 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:07 2024 GMT; NotAfter: Feb 20 17:51:07 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIED6TmQjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA3WhcNMjQwMjIwMTc1MTA3WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDG
ItRI0YQSg7GaQar1vRzAkcuAUsO/ZdTZtFmzkN6TyBt24ZrKKBWpLll6cDGt6+V/
G4w+kQpc3wRpfihFiudZxYahIsEoMvaSS3VsAKP1oeqOk6ya9l4v7wXZE/HnxmT/
N+rB/Fnpqo4Wxbi+nbIJSPU7xmK5BslH6RsJxveZOWmePnzVSkJbFmuj7EcLuYZV
asT1RoEYjkkNRM1+T7729Rv3ZkCF7S7AIV/9RobP+qUGWaweIcSIK73ZZwySaaYU
q087YDcrl+YteXLFJukqBLiDrl2QeBGjKnJ2JcNfGt8lgUDzGR85rZy/bJZuNNKG
2DIe6zfO4Qtd14aS1Hk1AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQDF
AbYvgfNCh6RFSe1tNefMqhZoywHtMdo2G1WGxGOgbXG0bJkjQ/BEHMeflkVmpv3A
/DoAGLW/ZO1VBgb9HImrYWDWGiXUo+cJxWiLLW9ewP6l1yCpOjPyT9DPUBzlKMdA
FFI3W0ehvIB6vv2YPvLsbgfDKWO+yh1OPZW+DQ0kAbIRiUlbuQrTYdK4mkckaj7h
oJQ93yBr80uGuErR+unKW2Vj0JI4KxglZVH9ekekbTBxNVqMkpnr2n/eEfnmFRuJ
IlAlXbdIC/5Fo0Llk/sERLUQA6FZ5eqykUvVeoJTj9kodi03AkNL2mxDTy1KaW+B
sPf9vsFkDW8mfXcNDFK2
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 8436E523E6F089F749B1EA6922F5A614A659E0E138F36CDE21512DC3C438A03A
    Session-ID-ctx:
    Resumption PSK: 3C751F98E08D9F19958BD3D71B7091AB0E1744258C470CA52CD1A671C695BE47E24DF9082045305431C8F17F89BDC1DE
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 67 62 ad 30 72 ef 35 8b-4b 97 68 8c 1c f3 24 79   gb.0r.5.K.h...$y
    0010 - 6f 54 de cd 5f 3a 5e c7-9e ce 92 82 00 bf cc 9f   oT.._:^.........
    0020 - fc e5 8d 2d 72 53 85 55-c0 27 41 b6 ef 02 bf 98   ...-rS.U.'A.....
    0030 - 72 bc 79 46 a1 52 64 21-ba fc 13 23 2d 4e 56 37   r.yF.Rd!...#-NV7
    0040 - 82 65 d1 5b 74 7d ea 9e-0a b9 33 f5 1f 2d 0d 29   .e.[t}....3..-.)
    0050 - 51 f1 8c fb bf 96 4c 10-c7 0a d8 12 f8 c5 4f a5   Q.....L.......O.
    0060 - 3d 8b 1d cf 0e cc ae e5-0f 90 00 f0 16 e3 dc 93   =...............
    0070 - 24 ee 08 4f 5a ff 22 39-d0 ce 58 ae e6 11 e0 8c   $..OZ."9..X.....
    0080 - 41 fb 1e a4 ae 94 20 da-56 cd 88 af 69 bd 71 8e   A..... .V...i.q.
    0090 - 05 26 a6 c8 02 b5 8d e5-44 65 1c 35 4c 28 ce 96   .&......De.5L(..
    00a0 - 90 15 63 e9 99 7f 81 0c-f6 fa a1 1a 66 10 73 98   ..c.........f.s.
    00b0 - 50 ea 9a 14 40 e4 e3 8a-1c 79 66 78 b2 83 8f a4   P...@....yfx....
    00c0 - 6c 23 65 1d 05 b5 f8 e4-1a 0d d0 24 7e 43 55 9c   l#e........$~CU.

    Start Time: 1708566435
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: B81E3D13DBC5E8BB4ABD61F47A9D486DF8396994B5E94CA787806E8A3337DEE7
    Session-ID-ctx:
    Resumption PSK: 9E45D47FD4EBD2E23830C94D2112B0ADCF20030F4080FAA822AAF6BA1B61DE1F993B19F80DCB3992710C735CDD3DDE00
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 67 62 ad 30 72 ef 35 8b-4b 97 68 8c 1c f3 24 79   gb.0r.5.K.h...$y
    0010 - 76 2f 98 9e 4e 84 d8 21-55 6a c8 41 71 a5 9f b3   v/..N..!Uj.Aq...
    0020 - 19 d5 49 01 63 97 91 5c-6e 44 60 08 75 32 20 06   ..I.c..\nD`.u2 .
    0030 - a5 ce 31 36 e5 4c dd 30-8a 67 f9 f0 c2 6a ce 7b   ..16.L.0.g...j.{
    0040 - 93 35 9f 0c a7 c3 6f 31-78 5d fe 3b 1d 32 61 7a   .5....o1x].;.2az
    0050 - f1 e2 60 af 89 b6 a2 39-c5 6a 93 47 e7 32 bd ea   ..`....9.j.G.2..
    0060 - ab 27 29 fa 58 90 38 f5-0b c8 64 03 7d f9 5b e4   .').X.8...d.}.[.
    0070 - 04 65 2a 22 dd 1c 40 f0-01 be f0 cc ad 92 d1 b1   .e*"..@.........
    0080 - f3 fe 08 c9 85 55 28 66-18 e7 4a dd 19 3f 6e d6   .....U(f..J..?n.
    0090 - 50 84 d2 73 bc 21 53 8b-35 4d a4 f3 e8 fb bd 3e   P..s.!S.5M.....>
    00a0 - 35 ff f8 0a 7a f2 2b 54-ff 4b 6d d9 be d9 4c 85   5...z.+T.Km...L.
    00b0 - 50 c4 d4 53 87 1e 27 f5-99 6c d2 e8 af 55 9d 9f   P..S..'..l...U..
    00c0 - a1 e3 86 a7 c4 3b 6f 0c-50 21 98 22 5a 4b 22 59   .....;o.P!."ZK"Y

    Start Time: 1708566435
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
JQttfApK4SeyHwDlI9SXGR50qclOAil1
^Z
[1]+  Stopped                 openssl s_client -connect localhost:31518
bandit16@bandit:~$ openssl s_client -connect localhost:31691
CONNECTED(00000003)
80DBF0F7FF7F0000:error:0A0000F4:SSL routines:ossl_statem_client_read_transition:unexpected message:../ssl/statem/statem_clnt.c:398:
---
no peer certificate available
---
No client certificate CA names sent
---
SSL handshake has read 293 bytes and written 300 bytes
Verification: OK
---
New, (NONE), Cipher is (NONE)
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 0 (ok)
---
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEQ9wEgDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDA
gdd50zQdwKnADuCYAoUSFvGreD2Mr/e6QZK+31XsKXCd/+cGHdmkqerggVlwno8T
3lmAaRw+Pk/nNdn3xJEGGq5guV2YhAnT+IQgP6+76ii/4gUCQxnaTtmslJDSfv7i
km+qYsFRL1YdtOo5od2etkLdorXGqGcIrB6ilCgKgQ2Q7FqMjh7n37HPk8yaWCwX
M/JZ7jkXw4mf2Un9UILgo/oJfR0JhMq6cDkHztG0E6j5ruknDeeOMGimH9pmzaa9
xdJe1GTtk+v03FIng0IfHi0HVPUCN8dl9rKLzn/LKZ3UftyffIErE7nDCLaGpVBK
DQzkq5gMPShGa1RT7nkFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBh
XmVUELbEPhoHaMrhwHyd24bRzYiiOemi75OA6QywOLh7moC8MGKvtI0mHhhA+lfB
eEvOOPwL5om4culG+KnC24fdWzwX/PPtkYKocNSrIQINrVhTwBbGwnC+WCSYizZS
43Zav+szrJ6H66qO4x4wXU9p1qC24dIpY5dfBsy4m8P/XzUtg68YJng1EIuGM6DF
CnMWXUB0cfUgBsbWPMrQlJd5sHifKeglK3kBCXn3zb9T881YbLNAwMK2a5SnPdh8
eTg1e7pdNYwPvHcxYPySGyQCkLpLHduWUxVNrUfsVHrxI6rrHynZ5vv4+ulAmhAc
YoU33/wx/D1oycw1GLHh
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 479E33F8FEB70F1CBD9E80EF9B623558257909068A2C8F95E0F6016AB7F21DED
    Session-ID-ctx:
    Resumption PSK: F48BA5D4F3F7139AC96997E3791D084AB3175541DDEEF5988DE521E828064C486C5B0A97979710AC437BFDFEE29B25DE
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - 9f f9 12 bc 2c 8a df b7-90 be fd 21 94 9a 9d 2f   ....,......!.../
    0020 - c8 70 f1 20 ff c6 0e 07-8a 4e a3 c6 91 13 e2 07   .p. .....N......
    0030 - 05 d8 60 85 fd a9 f4 3c-8f 9e 15 b0 e8 cd 03 12   ..`....<........
    0040 - 6d 4c a6 1b 49 a8 cf 89-44 0e 85 0f fc 2d da a3   mL..I...D....-..
    0050 - 50 ab fd e2 d9 80 d5 58-c3 77 ef 26 e9 ed 23 51   P......X.w.&..#Q
    0060 - 10 5e ff 11 3e a7 5e 54-dc ca 6e 58 91 c5 1d 20   .^..>.^T..nX...
    0070 - b1 ca 78 b4 1e 37 fd 5b-da 46 1e 35 80 02 4c 31   ..x..7.[.F.5..L1
    0080 - 2a 90 4e fb 6f 84 9e 48-e5 57 f0 1c a4 77 cb 90   *.N.o..H.W...w..
    0090 - 4c 8f 91 01 0e 21 f0 44-a8 2d 50 fc 81 d9 2d d6   L....!.D.-P...-.
    00a0 - 74 8f dd ad d5 49 1f 6a-30 f4 9f ac 1d 22 4d 45   t....I.j0...."ME
    00b0 - 20 c4 ed a6 87 2d 38 17-07 1a d6 d0 7d 14 fc 69    ....-8.....}..i
    00c0 - 67 48 c4 a9 46 98 5d 22-1b d1 80 d2 66 23 99 b2   gH..F.]"....f#..

    Start Time: 1708566493
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: DC88FA2409C49908EED2F392420FDEDB506C6930937AD40D83BF6AFC35C250FE
    Session-ID-ctx:
    Resumption PSK: 4AC9EEFA77E1B9F188871F3BC3D6DC399C50F590493B4D1C168C4C5A83B61C06B156BB5F519989824FA87814314B35A0
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - 4c e1 30 10 9c f9 31 66-3f 47 ae de 7c 65 e0 2c   L.0...1f?G..|e.,
    0020 - 4e 52 e3 86 2c d5 b9 3d-3c 48 14 a2 c8 c2 c8 df   NR..,..=<H......
    0030 - 09 37 a6 92 10 07 0a c0-4d f6 9a ae 2a df 53 0d   .7......M...*.S.
    0040 - 02 46 b1 1b cb c7 8a 0d-5b dc bb a2 8e b3 23 cd   .F......[.....#.
    0050 - 8d 1c 50 90 39 ae 94 73-10 d7 3e 5a 61 43 c1 f5   ..P.9..s..>ZaC..
    0060 - 0c 42 e8 97 b5 5a cf 9a-8c 6c 89 de 13 72 cd 71   .B...Z...l...r.q
    0070 - 96 0e c9 34 17 a1 1e c9-4b 62 73 f2 29 0f ea d9   ...4....Kbs.)...
    0080 - 12 7d a1 25 10 3f b6 b6-0e 7e a6 36 d0 63 98 2f   .}.%.?...~.6.c./
    0090 - f2 a1 b7 9a 49 8c d4 74-01 c2 ef a6 11 fb 4e 26   ....I..t......N&
    00a0 - 5d cf dd ae 63 3d 52 d8-f7 3f 16 05 5d 1e f9 c3   ]...c=R..?..]...
    00b0 - a2 1c b1 40 57 01 f8 c4-db ef 8d c3 a0 86 92 09   ...@W...........
    00c0 - 65 69 31 54 87 28 40 ea-7f ab de f1 77 b3 8a 95   ei1T.(@.....w...

    Start Time: 1708566493
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ exit

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/users/jho01/onedrive/escritorio/fsi]
└─$ ssh -i llaveLevel16-17.txt bandit17@bandit.labs.overthewire.org -p 2220

bandit17@bandit:~$ cd /
bandit17@bandit:/$ cd etc/
bandit17@bandit:/etc$ cd bandit_pass/
bandit17@bandit:/etc/bandit_pass$ cat bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```
## Notas adicionales

## Referencias
+ Ayuda del comando nmap