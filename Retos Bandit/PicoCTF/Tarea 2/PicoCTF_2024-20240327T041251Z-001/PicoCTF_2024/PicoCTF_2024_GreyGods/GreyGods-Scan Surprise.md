## Player: GreyGods
## Goal

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/3/challenge.zip)

Additional details will be available after launching your challenge instance.

## Hints
 + QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
 + Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
 + If you don't have access to a phone, you can also use zbar-tools to convert an image to text.

## Solution

```bash
oliva@kaioh:~$ ssh -p 51231 ctf-player@atlas.picoctf.net
 ssh -p 51231 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:51231 ([18.217.83.136]:51231)' can't be established.
ED25519 key fingerprint is SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:51231' (ED25519) to the list of known hosts.

ctf-player@atlas.picoctf.net's password:

ctf-player@challenge:~/drop-in$ Connection to atlas.picoctf.net closed by remote host.
Connection to atlas.picoctf.net closed.
````

+ I just had to use a qr scanner and read what was on the terminal and copy what I had decoded.
## Notes

## References