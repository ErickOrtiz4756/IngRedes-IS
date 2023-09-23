# Level 32 - Level 33
## Objetivo
After all this `git` stuff its time for another escape. Good luck!
## Datos de acceso al nivel
```bash
ssh bandit32@bandit.labs.overthewire.org -p 2220
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```
## Solución
```bash
>> ls
sh: 1: LS: Permission denied
>> $0
$ ls - la
ls: cannot access '-': No such file or directory
ls: cannot access 'la': No such file or directory
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Apr 23 18:04 uppershell
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
$ exit
```
## Notas adicionales
## Referencias