# Level 2- Level 3
## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
ssh bandit2@bandit.labs.overthewire.org -p 2220
bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
## Solución
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
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


Cuando hay un archivo con espacios para ver el contenido se pone entre comillas o en cada espacio poner una diagonal invertida
## Referencias
[Dealing With Spaces in Filenames in Linux (linuxhandbook.com)](https://linuxhandbook.com/filename-spaces-linux/)
