# Level 12 - Level 13
## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso al nivel
```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
## Solución
```bash
bandit12@bandit:~$ xxd -r data.txt | zcat |bzcat | zcat | tar xO | tar xO | bzcat | tar xO| zcat |  file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat |bzcat | zcat | tar xO | tar xO | bzcat | tar xO| zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales
Hay varias formas de desempaquetar un archivo, en este caso se usa el ver en consola para no hacerlo desde disco ya que es menos tardado
## Referencias
- [Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)