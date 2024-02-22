## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 18 10:54:16 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 18 10:54:16 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 18 10:53:16 2024 GMT; NotAfter: Feb 18 10:54:16 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEcjY6OTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjE4MTA1MzE2WhcNMjQwMjE4MTA1NDE2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCz
TX1NLedZhpQfXiWbWWD2BlNYjANpj+TnzUOI9ZbKJnOQJAbFfWZLA6No7XOStgje
+RPIoAHrX42G95VDfWtRms+qCsCTlUaS9291dZJQ3iOjBIE+PvmRcGdUlFJXDYa6
E61L2DKLbb8YSAnSuUPG3K7CtdxJpA5DpCBCmHEA9t5gZ5HGo9Gt9Kay9lhApX78
ocytwwHG15LplXI6LQB3ykhyCAcfljR3azd90T83dz7kLyM7yIMt60k1kemuX6RW
qSvkCvxmckRFoQPjwKZUopGLlhcC58Kb2xlwEGK+9j/ibBRkmEdBkOOeb5pJol7K
Wkd9LdG0nTWrggni7EKbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCA
j53OECoyjZMkHINZj35xk2kKQc9Jj9XjoCE0HlooUWd1ETik/2TkIbdWenozDrgH
10Jqmu/zAEhQkfFALBXCR7Vo0319yvR3rlnC2TdzMeBeUQ/n6ivPsCCL6SF8UTWT
XZJoTEfmp+Ma4zup/mEs23uO/FQ0J3LmSgICtXzPCA09M/ffj2UgTENdTHDltQxl
nQpzF+U40+bg/2PQ83XOTQJbZVbU2FnP/MitSYycxemLJXzbdsIxQhQy0VmTY73E
ZFemHVTbzEzcsCJRak4AyPZ9Zpi2uozHA8r1PqtnDzsN5FBFwuJxCuc+F8QeHh9e
QoyfsotkA6BO0LBqWNvE
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
    Session-ID: 033F7E3FD3E6DAD8F6318854BDAC8C4837EAEDA06999B94D8CAE0627BA11ECD4
    Session-ID-ctx: 
    Resumption PSK: 7F2D40F1C3EA118226B22AC9BF1F85D567977EB8B47BB8623B09D3B438321E68833C462D2C661467D4A44E45C520D469
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - dc 1b 67 7e 6b 49 ec f9-e1 0a 8a 6e cb ac b4 e6   ..g~kI.....n....
    0010 - c0 98 3d a1 8e ed b9 5c-0e 7e 4c fa 08 f5 d7 6c   ..=....\.~L....l
    0020 - e0 28 f7 b3 ec 70 4b e3-8b dc b9 a2 fd b8 24 22   .(...pK.......$"
    0030 - 11 5d 4b 81 79 4a fa 1f-e7 a0 cc ed cc 6f 63 46   .]K.yJ.......ocF
    0040 - 26 f7 95 c2 13 4b 46 03-75 c4 bf ab f8 e8 de 30   &....KF.u......0
    0050 - 85 f4 4e 94 61 1a dd 1a-4a 28 ba 4f 55 d2 82 03   ..N.a...J(.OU...
    0060 - 2b 17 bd 38 32 a2 ff c5-ca 52 a3 2f 5a 6a 86 4f   +..82....R./Zj.O
    0070 - c0 5f c5 b9 b2 63 40 20-a2 a0 f1 f7 60 3b ec f0   ._...c@ ....`;..
    0080 - a6 6a c2 66 f3 8e 06 b8-8a b0 0b 73 39 91 57 47   .j.f.......s9.WG
    0090 - c6 df e0 8b 89 39 e9 5e-c7 1d 70 2d 10 9d 40 bf   .....9.^..p-..@.
    00a0 - 78 64 f6 e5 2d 82 3d 59-ef c2 87 27 62 bc 42 0d   xd..-.=Y...'b.B.
    00b0 - 44 c6 a9 6b 19 b7 3b b1-aa ad 24 50 d0 d6 40 b8   D..k..;...$P..@.
    00c0 - ac a0 a4 11 36 8e 68 9d-97 05 4d 34 0c 94 29 5d   ....6.h...M4..)]

    Start Time: 1708370585
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
    Session-ID: BF9A8321F50F39176865F2CEEEE83560A4B5ACF79D29E1B36EB461CF44B78E15
    Session-ID-ctx: 
    Resumption PSK: 3D72F82E14772A9103D45DCDE3B96A3425BAE80B4FEDA2554664CB787787FFBE52878E2BBB5599203735022D5AAA5A8C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - dc 1b 67 7e 6b 49 ec f9-e1 0a 8a 6e cb ac b4 e6   ..g~kI.....n....
    0010 - 90 9b 57 e8 a1 6b 2c 5a-72 1f 2d 89 b3 7d 2a d8   ..W..k,Zr.-..}*.
    0020 - 53 63 a8 60 d8 69 a7 5d-32 21 eb 60 a9 d5 51 04   Sc.`.i.]2!.`..Q.
    0030 - 73 4c 66 1c 0a 06 25 c9-aa ea ca 22 ca a1 d5 37   sLf...%...."...7
    0040 - da b5 fa eb 6d f8 cd f8-7e 80 b0 86 70 7e 91 d6   ....m...~...p~..
    0050 - a4 1a 1c b2 4c bd 6d e8-c1 d7 0b b9 62 69 ad 44   ....L.m.....bi.D
    0060 - 7c 7e 23 7b b2 b4 4f 96-86 72 e0 aa ad eb db cb   |~#{..O..r......
    0070 - 2e ec ae 8c 73 c8 5f cf-03 8a 08 e3 42 f6 7e f9   ....s._.....B.~.
    0080 - 12 d0 fc 96 1b 35 26 b2-5a 33 77 69 99 b6 14 cb   .....5&.Z3wi....
    0090 - 1d 30 92 b1 e3 22 49 1f-b0 36 bf 5c 42 35 dd 49   .0..."I..6.\B5.I
    00a0 - ff 9d f9 89 d9 24 cb 33-7d 77 3f f0 04 b4 07 b1   .....$.3}w?.....
    00b0 - de 7a 44 07 b3 e0 5d 4b-07 8b 25 3a 62 2b c0 39   .zD...]K..%:b+.9
    00c0 - 67 8d 1b 71 10 cd 99 55-bb 5c fa 3a 97 61 f2 22   g..q...U.\.:.a."

    Start Time: 1708370585
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
```
## Notas adicionales

## Referencias