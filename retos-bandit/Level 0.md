# Level 0
## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit0
Password: bandit0
```
## Solución
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
## Notas adicionales
| **Comando** | **Descripción** |
|------------|--------------|
| pwd | Me indica el directorio actual |
| whoami | Saber el ususario actual |
| cd / | Me lleva al directorio raíz |
| exit | Cerrar sesión |
| clear o ctrl l | Limpiar pantalla |
| ls | Lista todas las carpetas del directorio actual |


## Referencias
- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)

## Comandos:
	pwd: 
		Saber en cual carpeta estoy
	clear o ctrl l: 
		limpiar pantalla
	whoami: 
		que usuario estoy usando
	 cd /: 
		 ir a la raíz
	ls o ls -la: 
		Listar carpetas 
	exit: 
		Salir de la sesión