## Objetivo
How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance
Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 52174
Username: picoplayer 
Password: bLgSMmbY6X
```
## Solución
```
picoplayer@challenge:/$ grep -r pico
grep: etc/.pwd.lock: Permission denied
etc/group:picoplayer:x:1000:
grep: etc/gshadow: Permission denied
etc/passwd:picoplayer:x:1000:1000::/home/picoplayer:/bin/bash
grep: etc/security/opasswd: Permission denied
grep: etc/shadow: Permission denied
etc/subgid:picoplayer:100000:65536
etc/subuid:picoplayer:100000:65536
grep: etc/ssh/ssh_host_ecdsa_key: Permission denied
grep: etc/ssh/ssh_host_ed25519_key: Permission denied
grep: etc/ssh/ssh_host_rsa_key: Permission denied
grep: etc/ssh/ssh_host_dsa_key: Permission denied
etc/crontab:# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1b4d8744}
... 
```
cabe destacar que después de la última línea que aparece en este código me aparecieron más, sin embargo, ya no tuvieron importancia, pues encontré la bandera
## Notas adicionales

## Referencias