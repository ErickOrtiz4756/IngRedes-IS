# Level 30 - Level 31
## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```bash
ssh bandit30@bandit.labs.overthewire.org -p 2220
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
## Solución
```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.dTkRDZiNaL
bandit30@bandit:~$ cd /tmp/tmp.dTkRDZiNaL
bandit30@bandit:/tmp/tmp.dTkRDZiNaL$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
bandit30@bandit:/tmp/tmp.dTkRDZiNaL$ ls
repo
bandit30@bandit:/tmp/tmp.dTkRDZiNaL$ cd repo
bandit30@bandit:/tmp/tmp.dTkRDZiNaL/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.dTkRDZiNaL/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.dTkRDZiNaL/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.dTkRDZiNaL/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Notas adicionales
## Referencias