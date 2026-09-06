## User & Group Access Management

```bash
rohit@Rohit-PC:~$ cd grinding
rohit@Rohit-PC:~/grinding$ ls
linux-day1
rohit@Rohit-PC:~/grinding$ mkdir linux-day2
rohit@Rohit-PC:~/grinding$ cd linux-day2
rohit@Rohit-PC:~/grinding/linux-day2$ ls
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 0
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupadd -g 1001 developers
[sudo] password for rohit:
groupadd: group 'developers' already exists
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupdel developers
groupdel: cannot remove the primary group of user 'alice'
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupadd -g 1001 coders
groupadd: GID '1001' already exists
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupadd -g 1002 coders
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupadd -g 1003 operations
rohit@Rohit-PC:~/grinding/linux-day2$ sudo groupadd -g 1004 database
rohit@Rohit-PC:~/grinding/linux-day2$ sudo useradd -g 1002 -m -s /bin/bash coder1
rohit@Rohit-PC:~/grinding/linux-day2$ sudo useradd -g 1002 -m -s /bin/bash coder2
rohit@Rohit-PC:~/grinding/linux-day2$ sudo useradd -g 1003 -m -s /bin/bash ops1
rohit@Rohit-PC:~/grinding/linux-day2$ sudo useradd -g 1004 -m -s /bin/bash db1
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 0
rohit@Rohit-PC:~$ cat /etc/passwd | grep -i 1002 1003 1004
grep: 1003: No such file or directory
grep: 1004: No such file or directory
rohit@Rohit-PC:~$ cat /etc/passwd | grep -i 1002
alice:x:1002:1001::/home/alice:/bin/bash
coder1:x:1004:1002::/home/coder1:/bin/bash
coder2:x:1005:1002::/home/coder2:/bin/bash
rohit@Rohit-PC:~$ cat /etc/passwd | grep -i 1003
bob:x:1003:1001::/home/bob:/bin/bash
ops1:x:1006:1003::/home/ops1:/bin/bash
rohit@Rohit-PC:~$ cat /etc/passwd | grep -i 1004
coder1:x:1004:1002::/home/coder1:/bin/bash
db1:x:1007:1004::/home/db1:/bin/bash
rohit@Rohit-PC:~$ cd grinding/linux-day2
rohit@Rohit-PC:~/grinding/linux-day2$ mkdir application shared
rohit@Rohit-PC:~/grinding/linux-day2$ ls
application  shared
rohit@Rohit-PC:~/grinding/linux-day2$ cd application
rohit@Rohit-PC:~/grinding/linux-day2/application$ mkdir coders operations database
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls
coders  database  operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxr-xr-x 2 rohit rohit 4096 Sep  5 06:34 coders
drwxr-xr-x 2 rohit rohit 4096 Sep  5 06:34 database
drwxr-xr-x 2 rohit rohit 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo chgrp coders coders
[sudo] password for rohit:
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxr-xr-x 2 rohit coders 4096 Sep  5 06:34 coders
drwxr-xr-x 2 rohit rohit  4096 Sep  5 06:34 database
drwxr-xr-x 2 rohit rohit  4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo chgrp database database
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo chgrp operations operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxr-xr-x 2 rohit coders     4096 Sep  5 06:34 coders
drwxr-xr-x 2 rohit database   4096 Sep  5 06:34 database
drwxr-xr-x 2 rohit operations 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 770 coders
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 770 database
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 770 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ cd ..
rohit@Rohit-PC:~/grinding/linux-day2$ ls
application  shared
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 8
drwxr-xr-x 5 rohit rohit 4096 Sep  5 06:34 application
drwxr-xr-x 2 rohit rohit 4096 Sep  5 06:34 shared
rohit@Rohit-PC:~/grinding/linux-day2$ chmod 777 shared
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 8
drwxr-xr-x 5 rohit rohit 4096 Sep  5 06:34 application
drwxrwxrwx 2 rohit rohit 4096 Sep  5 06:34 shared
rohit@Rohit-PC:~/grinding/linux-day2$ su -coder1
Password:
su: Authentication failure
rohit@Rohit-PC:~/grinding/linux-day2$ su - coder1
Password:
su: Authentication failure
rohit@Rohit-PC:~/grinding/linux-day2$ sudo su - coder1
/home/coder1/.hushlogin file.
coder1@Rohit-PC:~$ ls
coder1@Rohit-PC:~$ ls -l
total 0
coder1@Rohit-PC:~$ cd coders
-bash: cd: coders: No such file or directory
coder1@Rohit-PC:~$ exit
logout
rohit@Rohit-PC:~/grinding/linux-day2$ cd ..
rohit@Rohit-PC:~/grinding$ cd ..
rohit@Rohit-PC:~$ ls -l
total 136
drwxr-xr-x 2 rohit rohit  4096 Aug  6 11:26  6-8-2026
drwxr-xr-x 3 rohit rohit  4096 Jul 29 05:18  LINUX_PRACTICE
-rw-r--r-- 1 rohit rohit    15 Aug 18 06:41  app.txt
-rw-r--r-- 1 rohit rohit 10240 Aug  5 12:58  backup.tar
-rw-r--r-- 1 rohit rohit   118 Aug  5 13:00  backup.tar.gz
-rw-r--r-- 1 rohit rohit 10240 Aug  5 12:56  backup.tat
-rw-r--r-- 1 rohit rohit     0 Aug  3 11:39  chapter3
drwxr-xr-x 4 rohit rohit  4096 Aug 25 12:19  cloud-lab
-rw-r--r-- 1 root  root      0 Aug 18 06:40  config.txt
-rw-r--r-- 1 rohit rohit    52 Aug  4 07:14  file1.txt
-rw-r--r-- 1 rohit rohit    52 Aug  4 07:15  file2.txt
drwxr-xr-x 4 rohit rohit  4096 Sep  5 06:12  grinding
-rw-r--r-- 1 rohit rohit    46 Aug  1 05:29 'learning quote'
drwxr-xr-x 5 rohit rohit  4096 Aug 18 09:15  linux-project
-rw-r--r-- 1 rohit rohit    54 Jul 31 10:33  listOfFiles
drwxr-xr-x 2 rohit rohit  4096 Aug  4 10:19  new
-rw-r--r-- 1 rohit rohit    17 Aug  6 10:21  notes.txt
drwxr-xr-x 2 rohit rohit  4096 Aug  4 10:19  old
-rw-r--r-- 1 rohit rohit    52 Aug 12 12:11  order.txt
-rw-r--r-- 1 rohit rohit    67 Jul 31 10:54  output
drwxr-xr-x 3 rohit rohit  4096 Jul 29 12:25  podman-node-demo
-rw-r--r-- 1 rohit rohit   193 Aug  1 07:14  practice
-rw-r--r-- 1 rohit rohit    46 Aug  1 05:30  quote
drwxr-xr-x 5 rohit rohit 16384 Aug 30 14:41  shell-scripting
lrwxrwxrwx 1 rohit rohit     5 Aug  5 10:43  shortcut -> file1
-rw-r--r-- 1 rohit rohit     0 Jul 31 13:20  t.text
drwxr-xr-x 2 rohit rohit  4096 Aug  5 12:57  tarpractice
drwxr-xr-x 2 rohit rohit  4096 Aug  4 09:17  tempbackup
drwxr-xr-x 2 rohit rohit  4096 Jul 28 08:53  temporary
-rw-r--r-- 1 rohit rohit    39 Aug  1 07:24  testfile
drwxr-xr-x 2 rohit rohit  4096 Aug 15 07:34  wild
rohit@Rohit-PC:~$ chgrp coders grinding
chgrp: changing group of 'grinding': Operation not permitted
rohit@Rohit-PC:~$ sudo chgrp coders grinding
rohit@Rohit-PC:~$ cd grinding
rohit@Rohit-PC:~/grinding$ ls -l
total 8
drwxr-xr-x 5 rohit rohit 4096 Sep  2 06:13 linux-day1
drwxr-xr-x 4 rohit rohit 4096 Sep  5 06:34 linux-day2
rohit@Rohit-PC:~/grinding$ sudo chgrp coders linux-day2
rohit@Rohit-PC:~/grinding$ ls -l
total 8
drwxr-xr-x 5 rohit rohit  4096 Sep  2 06:13 linux-day1
drwxr-xr-x 4 rohit coders 4096 Sep  5 06:34 linux-day2
rohit@Rohit-PC:~/grinding$ cd ..
rohit@Rohit-PC:~$ ls -l
rohit@Rohit-PC:~$ chmod 770 grinding
rohit@Rohit-PC:~$ cd grinding
rohit@Rohit-PC:~/grinding$ ls -l
total 8
drwxr-xr-x 5 rohit rohit  4096 Sep  2 06:13 linux-day1
drwxr-xr-x 4 rohit coders 4096 Sep  5 06:34 linux-day2
rohit@Rohit-PC:~/grinding$ chmod 770 linux-day2
rohit@Rohit-PC:~/grinding$ ls -l
total 8
drwxr-xr-x 5 rohit rohit  4096 Sep  2 06:13 linux-day1
drwxrwx--- 4 rohit coders 4096 Sep  5 06:34 linux-day2
rohit@Rohit-PC:~/grinding$ cd linux-day2
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 8
drwxr-xr-x 5 rohit rohit 4096 Sep  5 06:34 application
drwxrwxrwx 2 rohit rohit 4096 Sep  5 06:34 shared
rohit@Rohit-PC:~/grinding/linux-day2$ sudo chgrp coders applications
chgrp: cannot access 'applications': No such file or directory
rohit@Rohit-PC:~/grinding/linux-day2$ sudo chgrp coders application
rohit@Rohit-PC:~/grinding/linux-day2$ chmod 770 applications
chmod: cannot access 'applications': No such file or directory
rohit@Rohit-PC:~/grinding/linux-day2$ chmod 770 application
rohit@Rohit-PC:~/grinding/linux-day2$ ls -l
total 8
drwxrwx--- 5 rohit coders 4096 Sep  5 06:34 application
drwxrwxrwx 2 rohit rohit  4096 Sep  5 06:34 shared
rohit@Rohit-PC:~/grinding/linux-day2$ cd application
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxrwx--- 2 rohit coders     4096 Sep  5 06:34 coders
drwxrwx--- 2 rohit database   4096 Sep  5 06:34 database
drwxrwx--- 2 rohit operations 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo su - coder1
coder1@Rohit-PC:~$ ls
coder1@Rohit-PC:~$ ls -l
total 0

rohit@Rohit-PC:~$ cd grinding
rohit@Rohit-PC:~/grinding$ ls
linux-day1  linux-day2
rohit@Rohit-PC:~/grinding$ cd linux-day2
rohit@Rohit-PC:~/grinding/linux-day2$ ls
application  shared
rohit@Rohit-PC:~/grinding/linux-day2$ cd applications
-bash: cd: applications: No such file or directory
rohit@Rohit-PC:~/grinding/linux-day2$ cd application
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls
coders  database  operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ cd coders
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ ls
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ cat file1.txt
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ echo "This file created by Rohit" >> file1.txt
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ cat file1.txt
This file created by Rohit
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ su - coder1
Password:
^C
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ sudo su - coder1
coder1@Rohit-PC:~$ cd home/rohit/grinding/linux-day2/application/coders
-bash: cd: home/rohit/grinding/linux-day2/application/coders: No such file or directory
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
-bash: cd: /home/rohit/grinding/linux-day2/application/coders: Permission denied
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
-bash: cd: /home/rohit/grinding/linux-day2/application/coders: Permission denied
coder1@Rohit-PC:~$ exit
logout
'rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ 'cd
>
> ^C
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ cd
rohit@Rohit-PC:~$ cd ..
rohit@Rohit-PC:/home$ ls
alice  bob  coder1  coder2  db1  jaibabu  ops1  rohit
rohit@Rohit-PC:/home$ chmod 755 rohit
rohit@Rohit-PC:/home$ ls -l
total 32
drwxr-x---  2 alice   developers 4096 Aug 18 07:17 alice
drwxr-x---  2 bob     developers 4096 Aug 18 07:18 bob
drwxr-x---  3 coder1  coders     4096 Sep  5 07:02 coder1
drwxr-x---  2 coder2  coders     4096 Sep  5 06:22 coder2
drwxr-x---  2 db1     database   4096 Sep  5 06:23 db1
drwxr-x---  2 jaibabu rohit      4096 Aug 17 17:15 jaibabu
drwxr-x---  2 ops1    operations 4096 Sep  5 06:23 ops1
drwxr-xr-x 18 rohit   rohit      4096 Sep  2 06:12 rohit
rohit@Rohit-PC:/home$ cd
rohit@Rohit-PC:~$ cd grinding/linux-day2/application/coders
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ su - coder1
Password:
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ sudo su - coder1
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ ls
'This file created by Rohit'   file1.txt
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ echo "This file created by coder1" >> file2.txt
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ cat file2.txt
This file created by coder1
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ exit
logout
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ ls
'This file created by Rohit'   file1.txt   file2.txt
rohit@Rohit-PC:~/grinding/linux-day2/application/coders$ cd ..
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls
coders  database  operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxrwx--- 2 rohit coders     4096 Sep  6 10:15 coders
drwxrwx--- 2 rohit database   4096 Sep  5 06:34 database
drwxrwx--- 2 rohit operations 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 774 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo su - coder1
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ cd ..
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ ls -l
total 12
drwxrwx--- 2 rohit coders     4096 Sep  6 10:15 coders
drwxrwx--- 2 rohit database   4096 Sep  5 06:34 database
drwxrwxr-- 2 rohit operations 4096 Sep  5 06:34 operations
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ cd operations
-bash: cd: operations: Permission denied
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ chmod 774 database
chmod: changing permissions of 'database': Operation not permitted
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ exit
logout
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxrwx--- 2 rohit coders     4096 Sep  6 10:15 coders
drwxrwx--- 2 rohit database   4096 Sep  5 06:34 database
drwxrwxr-- 2 rohit operations 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 774 databse
chmod: cannot access 'databse': No such file or directory
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 774 database
rohit@Rohit-PC:~/grinding/linux-day2/application$ ls -l
total 12
drwxrwx--- 2 rohit coders     4096 Sep  6 10:15 coders
drwxrwxr-- 2 rohit database   4096 Sep  5 06:34 database
drwxrwxr-- 2 rohit operations 4096 Sep  5 06:34 operations
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo su - coder1
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ cd ..
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ cd database
-bash: cd: database: Permission denied
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ exit
logout
rohit@Rohit-PC:~/grinding/linux-day2/application$ chmod 775 database
rohit@Rohit-PC:~/grinding/linux-day2/application$ sudo su - coder1
coder1@Rohit-PC:~$ cd /home/rohit/grinding/linux-day2/application/coders
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application/coders$ cd ..
coder1@Rohit-PC:/home/rohit/grinding/linux-day2/application$ cd database
```