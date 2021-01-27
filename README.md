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
* - regular file
* d directory
* l symbolik link file
* c special file
* s Socket
* p Named pipe
* b Block device

# Daftar Pustaka
http://www.porcupine.org/forensics/forensic-discovery/
