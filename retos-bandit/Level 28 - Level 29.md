# Level 29 - Level 29
## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.
## Datos de acceso al nivel
```bash
ssh bandit28@bandit.labs.overthewire.org -p 2220
AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
## Solución
```bash
bandit28@bandit:~$ mktemp -d
/tmp/tmp.EQELGpNcHp
bandit28@bandit:~$ cd /tmp/tmp.EQELGpNcHp
bandit28@bandit:/tmp/tmp.EQELGpNcHp$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
bandit28@bandit:/tmp/tmp.EQELGpNcHp$ ls
repo
bandit28@bandit:/tmp/tmp.EQELGpNcHp$ cd repo
bandit28@bandit:/tmp/tmp.EQELGpNcHp/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.EQELGpNcHp/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.EQELGpNcHp/repo$ git log
commit 899ba88df296331cc01f30d022c006775d467f28 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    fix info leak

commit abcff758fa6343a0d002a1c0add1ad8c71b88534
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    add missing data

commit c0a8c3cf093fba65f4ee0e1fe2a530b799508c78
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/tmp.EQELGpNcHp/repo$ git show 899ba88df296331cc01f30d022c006775d467f28
commit 899ba88df296331cc01f30d022c006775d467f28 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.EQELGpNcHp/repo$
```
## Notas adicionales
Usar git log para mostrar el historial de commits y git show para ver el commit especifico
## Referencias