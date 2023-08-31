# Level 6 - Level 7
## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Solución
```bash
bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Notas adicionales
Usar find para encontrar archivos especificos como -size 33c -user bandit7 -group bandit6 2>/dev/null
## Referencias
