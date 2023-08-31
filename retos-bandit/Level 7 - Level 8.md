# Level 7 - Level 8
## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Solución
```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Notas adicionales
Grep busca patrones en archivos, puedes especificar esos patrones y en cuales archivos buscar
## Referencias
