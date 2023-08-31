# Level 3 - Level 4
## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Solución

```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```
## Notas adicionales
|**Comando**|**Descripción**|
|---|---|
|pwd|Me indica el directorio actual|
|whoami|Saber el ususario actual|
|cd /|Me lleva al directorio raíz|
|exit|Cerrar sesión|
|clear o ctrl l|Limpiar pantalla|
|ls|Lista todas las carpetas del directorio actual|
|cat|Muestra el contenido del archivo seleccionado|

Para mostrar archivos ocultos usar ls -a o ls -la
## Referencias
