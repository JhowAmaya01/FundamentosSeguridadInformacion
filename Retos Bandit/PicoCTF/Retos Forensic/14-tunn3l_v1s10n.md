## Objetivo

## Solución
```
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ls
tunn3l_v1s10n
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ file tunn3l_v1s10n                                          
tunn3l_v1s10n: data
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ls -la
total 3604
drwxr-xr-x 3 kali kali   28672 mar 30 22:29 .
drwxr-xr-x 4 kali kali    4096 mar 30 22:29 ..
-rw-r--r-- 1 kali kali 2893454 mar 30 22:29 tunn3l_v1s10n
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ exiftool tunn3l_v1s10n 
ExifTool Version Number         : 12.49
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:03:30 22:29:27-06:00
File Access Date/Time           : 2023:03:30 22:29:48-06:00
File Inode Change Date/Time     : 2023:03:30 22:29:48-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Unknown (53434)
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Red Mask                        : 0x27171a23
Green Mask                      : 0x20291b1e
Blue Mask                       : 0x1e212a1d
Alpha Mask                      : 0x311a1d26
Color Space                     : Unknown (,5%()
Rendering Intent                : Unknown (826103054)
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open tunn3l_v1s10n          
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ** Message: 22:36:18.095: Could not open file 'file:///home/kali/Descargas/Forensic/tunn3l_v1s10n': Tipo MIME no compatible
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ls    
capture.pcap  _dolls.jpg.extracted  tunn3l_v1s10n
dolls.jpg     picopico.key
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ mv tunn3l_v1s10n tunn3l_v1s10n.bmp
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ file tunn3l_v1s10n.bmp 
tunn3l_v1s10n.bmp: data
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ** Message: 22:37:32.761: Could not open file 'file:///home/kali/Descargas/Forensic/tunn3l_v1s10n.bmp': Tipo MIME no compatible
    
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ xxd -l 16 tunn3l_v1s10n.bmp
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
                                                                 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ hexeditor tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ ** Message: 22:42:20.317: Could not open file 'file:///home/kali/Descargas/Forensic/tunn3l_v1s10n.bmp': Tipo MIME no compatible
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ file tunn3l_v1s10n.bmp 
tunn3l_v1s10n.bmp: data
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 12.49
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:03:30 22:42:03-06:00
File Access Date/Time           : 2023:03:30 22:42:04-06:00
File Inode Change Date/Time     : 2023:03:30 22:42:03-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Unknown (53288)
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Red Mask                        : 0x27171a23
Green Mask                      : 0x20291b1e
Blue Mask                       : 0x1e212a1d
Alpha Mask                      : 0x311a1d26
Color Space                     : Unknown (,5%()
Rendering Intent                : Unknown (826103054)
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ file tunn3l_v1s10n.bmp 
tunn3l_v1s10n.bmp: PC bitmap, Windows 3.x format, 1134 x 306 x 24, image size 2893400, resolution 5669 x 5669 px/m, cbSize 2893454, bits offset 40
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 12.49
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:03:30 22:43:22-06:00
File Access Date/Time           : 2023:03:30 22:44:04-06:00
File Inode Change Date/Time     : 2023:03:30 22:43:22-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ hexeditor tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open t                
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ open tunn3l_v1s10n.bmp 
                                                                 
┌──(kali㉿kali)-[~/Descargas/Forensic]
└─$ 

```
## Notas adicionales

## Referencias
