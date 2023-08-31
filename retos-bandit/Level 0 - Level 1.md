# Level 0 - Level 1
## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
## Datos de acceso al nivel
Server: bandit.labs.overthewire.org
User: bandit0
Password: bandit0
## Solución
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
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
|cat | Muestra el contenido del archivo seleccionado |

## Referencias
