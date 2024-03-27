## Objetivo
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 62817`

## Solución

``` bash
aers-picoctf@webshell:~/interencdec$ ls
enc_flag
aers-picoctf@webshell:~/interencdec$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==
aers-picoctf@webshell:~/interencdec$ echo 'YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==' | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2kyMDRoa2o2fQ=='
aers-picoctf@webshell:~/interencdec$ echo 'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2kyMDRoa2o2fQ==' | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_i204hkj6}

picoCTF{caesar_d3cr9pt3d_b204adc6}

```

## Referencias
https://www.base64decode.org/es/
https://www.dcode.fr/rot-cipher
