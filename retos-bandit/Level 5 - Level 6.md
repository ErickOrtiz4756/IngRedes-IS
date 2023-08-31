# Level 5 - Level 6
## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
## Datos de acceso al nivel
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
## Solución
```bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Notas adicionales
Usar find para encontrar un archivo especifico
## Referencias
