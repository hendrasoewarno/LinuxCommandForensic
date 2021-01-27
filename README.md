# LinuxCommandForensic
Berikut ini adalah beberapa perintah Linux yang digunakan untuk pemeriksaan Forensic penyerangan
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
# File pada Linux
Pada prinsipnya Linux memperlakukan Directory sama dengan file biasa, perbedaannya adalah Directory adalah suatu file yang berisi daftar nama Directory ataupun file lainnya.
## jenis File
Ketika anda memberikan perintah ls -l, maka akan ditampilkan daftar file, sesuatu hal yang perlu anda perhatikan adalah jenis file yang mungkin pada Linux. Pada umumnya kita hanya memperhatikan jenis file yang berupa (- regular file, d directory, dan l symbolic link file), tetapi sebenarnya pada Linux masih terdapat beberapa jenis file lainnya:
* \- regular file
* d directory
* l symbolik link file
* c special file
* s Socket
* p Named pipe
* b Block device
## status pada file
Mendapatkan Modify, Access, dan Create time pada suatu file/directory dapat menggunakan perintah stat <nama file/directory>
```
stat test.py

stat test.py
  File: 'test.py'
  Size: 4096            Blocks: 8          IO Block: 4096   directory
Device: 802h/2050d      Inode: 4736978     Links: 5
Access: (0755/drwxr-xr-x)  Uid: ( 1003/user001)   Gid: ( 1003/user001)
Access: 2021-01-27 15:45:54.146414112 +0700
Modify: 2019-04-24 10:45:53.582765182 +0700
Change: 2019-04-24 10:45:53.582765182 +0700

```
# Daftar Pustaka
http://www.porcupine.org/forensics/forensic-discovery/
