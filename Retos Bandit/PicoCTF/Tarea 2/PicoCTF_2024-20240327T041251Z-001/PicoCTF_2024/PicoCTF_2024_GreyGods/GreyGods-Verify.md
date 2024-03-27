## Player: GreyGods
## Goal
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.You can download the challenge files here:

- `[challenge.zip](https://artifacts.picoctf.net/c_rhea/12/challenge.zip)`

The same files are accessible via SSH here:`ssh -p 50519 ctf-player@rhea.picoctf.net`Using the password `6dd28e9b`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

- Checksum: 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8
- To decrypt the file once you've verified the hash, run `./decrypt.sh files/<file>`.
## Solution

```bash
ssh -p 50519 ctf-player@rhea.picoctf.net
──(kali㉿kali)-[~]
└─$ ssh -p 50519 ctf-player@rhea.picoctf.net
The authenticity of host '[rhea.picoctf.net]:50519 ([3.136.191.228]:50519)' can't be established.
ED25519 key fingerprint is SHA256:QKdv+RGJL0UYRDM66IiGQ5dsXOX7DQFqB7umTylh+IU.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[rhea.picoctf.net]:50519' (ED25519) to the list of known hosts.
ctf-player@rhea.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1014-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$ ls
checksum.txt  decrypt.sh  files
ctf-player@pico-chall$ cat checksum.txt 
03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8
ctf-player@pico-chall$ sha256sum files/* | grep 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8
03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8  files/00011a60
ctf-player@pico-chall$ cat files/00011a60
Salted__^PI�h���yp�&��?�}��a�|�K
▒\�t��ꌘ�ð��p������ctf-player@pico-chall$ ./decrypt.sh files/00011a60 
picoCTF{trust_but_verify_00011a60}

````


## Notes

## References