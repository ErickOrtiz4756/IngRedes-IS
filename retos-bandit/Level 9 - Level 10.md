# Level 9 - Level 10
## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Solución
```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ cat data.txt | strings -n 20
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas adicionales
String, comando para obtener lineas de caracteres y con -n puedes especificar cuantos caracteres tiene
## Referencias
