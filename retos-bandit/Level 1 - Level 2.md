# Level 1 - Level 2
## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel
```
ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
## Solución
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
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

Cuando un archivo comienza con un guion tenemos que anteponer ./ al nombre o especificar la ruta completa al archivo
## Referencias
- [linux - How to open a "-" dashed filename using terminal? - Stack Overflow](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)
- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)
