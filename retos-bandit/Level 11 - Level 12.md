# Level 11 - Level 12
## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel
```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
## Solución
```bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
## Notas adicionales
tr es un comando para rotar los caracteres 13 veces que se usa para codificar
## Referencias
- [Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)