## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
## Solución
```
git clone https://github.com/colaclanth/sstv.git
python setup.py install

C:\Users\jho01\Downloads\pico\actividad 9>sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [######################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!

C:\Users\jho01\Downloads\pico\actividad 9>dir
 El volumen de la unidad C no tiene etiqueta.
 El número de serie del volumen es: 3592-FAA2

 Directorio de C:\Users\jho01\Downloads\pico\actividad 9

28/03/2023  08:27 a. m.    <DIR>          .
28/03/2023  08:27 a. m.    <DIR>          ..
28/03/2023  08:12 a. m.        11,066,998 message.wav
28/03/2023  08:27 a. m.           200,716 result.png
               2 archivos     11,267,714 bytes
               2 dirs  720,075,177,984 bytes libres

C:\Users\jho01\Downloads\pico\actividad 9>result.png
```
picoCTF{beep_boop_im_in_space}
## Notas adicionales

## Referencias
