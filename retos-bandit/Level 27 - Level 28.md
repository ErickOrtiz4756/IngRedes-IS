# Level 27 - Level 28
## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```bash
ssh bandit27@bandit.labs.overthewire.org -p 2220
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```
## Solución
```bash
bandit27@bandit:~$ mktemp -d
/tmp/tmp.GIj9kael1k
bandit27@bandit:~$ cd /tmp/tmp.GIj9kael1k
bandit27@bandit:/tmp/tmp.GIj9kael1k$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
bandit27@bandit:/tmp/tmp.GIj9kael1k$ ls
repo
bandit27@bandit:/tmp/tmp.GIj9kael1k$ cd repo
bandit27@bandit:/tmp/tmp.GIj9kael1k/repo$ ls
README
bandit27@bandit:/tmp/tmp.GIj9kael1k/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR

```
## Notas adicionales
## Referencias