# Level 8 - Level 9
## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Solución
```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```
## Notas adicionales
Usando piping utilizar sort para acomodar el contenido de un archivo y despues usar uniq para que muestre el que no se repite
## Referencias
[Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)

