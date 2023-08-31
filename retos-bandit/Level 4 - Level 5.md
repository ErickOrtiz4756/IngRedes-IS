# Level 4 - Level 5
## Objetivo
## Datos de acceso al nivel
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```


## Solución
```bash
bandit4@bandit:~/inhere$ ls -la
bandit4@bandit:~/inhere$ file ./-file00
./-file00: data
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: Non-ISO extended-ASCII text, with no line terminators
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

## Notas adicionales
Utilizar el comando file para ver que contiene el archivo y usar un * para abrir o ver todos los archivos
## Referencias
