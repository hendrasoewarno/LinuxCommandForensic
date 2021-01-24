# LinuxCommandForensic
Berikut ini adalah beberapa perintah Linux yang digunakan untuk pemeriksaan Forensic penyerangan
## who
Mendapatkan daftar user yang sedang login ke system
## lsof
Mendapatkan file yang dibuka oleh suatu ipaddress, process id, ataupun file yang terbuka pada device tertentu.
```
date
uptime
uname -a
ifconfig
#show who is currently login
w
#list all process
ps -eaf
#list listened TCP connection
netstat -at
#list listened UDP connection
netstat -au
#open file by ipV4
lsof -4
#open file by pid
lsof -p <pid>
#opened file but deleted
lsof -L1
which passwd
#check for set UID or set GID
ls -l /usr/bin/passwd
#find file with set UID and ignore error
find / -uid 0 -perm -4000 2>/dev/null
#find file with set GID and ignore error
find / -uid 0 -perm -2000 2>/dev/null

date

```
