# Level 29 - Level 30
## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```bash
ssh bandit29@bandit.labs.overthewire.org -p 2220
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```
## Solución
```bash
bandit29@bandit:~$ mktemp -d
/tmp/tmp.vwBGX9j8Am
bandit29@bandit:~$ cd /tmp/tmp.vwBGX9j8Am
bandit29@bandit:/tmp/tmp.vwBGX9j8Am$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
bandit29@bandit:/tmp/tmp.vwBGX9j8Am$ ls
repo
bandit29@bandit:/tmp/tmp.vwBGX9j8Am$ cd repo
bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ ls -la
total 20
drwxrwxr-x 4 bandit29 bandit29 4096 Sep 23 04:40 .
drwx------ 3 bandit29 bandit29 4096 Sep 23 04:39 ..
drwxrwxr-x 2 bandit29 bandit29 4096 Sep 23 04:40 code
drwxrwxr-x 8 bandit29 bandit29 4096 Sep 23 04:40 .git
-rw-rw-r-- 1 bandit29 bandit29  134 Sep 23 04:40 README.md
bandit29@bandit:/tmp/tmp.vwBGX9j8Am/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
## Notas adicionales
Usar git branch para verificar si hay mas branches y git checkout para cambiar de branch
## Referencias