# Level 31 - Level 32
## Objetivo
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```bash
ssh bandit31@bandit.labs.overthewire.org -p 2220
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Solución
```bash
bandit31@bandit:~$ mktemp -d
/tmp/tmp.ifnw8zWRTk
bandit31@bandit:~$ cd /tmp/tmp.ifnw8zWRTk
bandit31@bandit:/tmp/tmp.ifnw8zWRTk$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
bandit31@bandit:/tmp/tmp.ifnw8zWRTk$ ls
repo
bandit31@bandit:/tmp/tmp.ifnw8zWRTk$ cd repo
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ echo 'May I come in?' > key.txt
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ git add -f key.txt
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ git commit -a
[master fab33b3] okgokgkgkokkokg
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$ git push -u origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 324 bytes | 162.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/tmp.ifnw8zWRTk/repo$
```
## Notas adicionales
## Referencias