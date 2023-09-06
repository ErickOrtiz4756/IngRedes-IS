# Level 10 - Level 11
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Solución
```bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```


## Notas adicionales
Usar base64 para decodificar o codificar, en este caso decodifica los datos del archivo nombrado data.txt
## Referencias
- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)