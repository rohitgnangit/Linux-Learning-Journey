### Practice 1 :
- Application Server File Management & Log Backup
```bash
rohit@Rohit-PC:~$ cd grinding
rohit@Rohit-PC:~/grinding$ mkdir linux-day1
rohit@Rohit-PC:~/grinding$ cd linux-day1
rohit@Rohit-PC:~/grinding/linux-day1$ mkdir app backup tmp
rohit@Rohit-PC:~/grinding/linux-day1$ ls
app  backup  tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd app
rohit@Rohit-PC:~/grinding/linux-day1/app$ touch config logs data
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
config  data  logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd config
-bash: cd: config: Not a directory
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
config  data  logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ rm *
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
rohit@Rohit-PC:~/grinding/linux-day1/app$ mkdir config logs data
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
config  data  logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ touch app.config database.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ ls
app.config  database.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd logs
rohit@Rohit-PC:~/grinding/linux-day1/app/logs$ touch app.log error.log access.log
rohit@Rohit-PC:~/grinding/linux-day1/app/logs$ ls
access.log  app.log  error.log
rohit@Rohit-PC:~/grinding/linux-day1/app/logs$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd data
rohit@Rohit-PC:~/grinding/linux-day1/app/data$ touch users.txt products.txt
rohit@Rohit-PC:~/grinding/linux-day1/app/data$ ls
products.txt  users.txt
rohit@Rohit-PC:~/grinding/linux-day1/app/data$ cd..
cd..: command not found
rohit@Rohit-PC:~/grinding/linux-day1/app/data$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ cd tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ touch test1.tmp test2.tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ ls
test1.tmp  test2.tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ find *.log
find: ‘*.log’: No such file or directory
rohit@Rohit-PC:~/grinding/linux-day1$ find /logs/*.log
find: ‘/logs/*.log’: No such file or directory
rohit@Rohit-PC:~/grinding/linux-day1$ find . -name "*.log"
./app/logs/access.log
./app/logs/app.log
./app/logs/error.log
rohit@Rohit-PC:~/grinding/linux-day1$ find . -name "*.config"
./app/config/app.config
./app/config/database.config
rohit@Rohit-PC:~/grinding/linux-day1$ find . -name "*.tmp"
./tmp/test1.tmp
./tmp/test2.tmp
rohit@Rohit-PC:~/grinding/linux-day1$ find . -type f
./app/config/app.config
./app/config/database.config
./app/logs/access.log
./app/logs/app.log
./app/logs/error.log
./app/data/products.txt
./app/data/users.txt
./tmp/test1.tmp
./tmp/test2.tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd app/config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ ls -l
total 0
-rw-r--r-- 1 rohit rohit 0 Sep  2 06:16 app.config
-rw-r--r-- 1 rohit rohit 0 Sep  2 06:16 database.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ cdmod 640 app.config
Command 'cdmod' not found, did you mean:
  command 'chmod' from deb coreutils (9.4-3ubuntu6.2)
Try: sudo apt install <deb name>
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ chmod 640 app.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ chmod 640 database.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ ls -l
total 0
-rw-r----- 1 rohit rohit 0 Sep  2 06:16 app.config
-rw-r----- 1 rohit rohit 0 Sep  2 06:16 database.config
rohit@Rohit-PC:~/grinding/linux-day1/app/config$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1/app$ whoami
rohit
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ ls -l
total 12
drwxr-xr-x 5 rohit rohit 4096 Sep  2 06:15 app
drwxr-xr-x 2 rohit rohit 4096 Sep  2 06:13 backup
drwxr-xr-x 2 rohit rohit 4096 Sep  2 06:18 tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd app
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls -l
total 12
drwxr-xr-x 2 rohit rohit 4096 Sep  2 06:16 config
drwxr-xr-x 2 rohit rohit 4096 Sep  2 06:17 data
drwxr-xr-x 2 rohit rohit 4096 Sep  2 06:16 logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ ls
app  backup  tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd app
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
config  data  logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ tar /grinding/linux-day1/backup logs
tar: Old option 'g' requires an argument.
Try 'tar --help' or 'tar --usage' for more information.
rohit@Rohit-PC:~/grinding/linux-day1/app$ tar grinding/linux-day1/backup log
s
tar: Old option 'g' requires an argument.
Try 'tar --help' or 'tar --usage' for more information.
rohit@Rohit-PC:~/grinding/linux-day1/app$ tar -cvf /grinding/linux-day1/back
up logs
tar: /grinding/linux-day1/backup: Cannot open: No such file or directory
tar: Error is not recoverable: exiting now
rohit@Rohit-PC:~/grinding/linux-day1/app$ tar -cvf ~/grinding/linux-day1/bac
kup logs
tar: /home/rohit/grinding/linux-day1/backup: Cannot open: Is a directory
tar: Error is not recoverable: exiting now
rohit@Rohit-PC:~/grinding/linux-day1/app$ tar -cvf ~/grinding/linux-day1/backup/backup.tar logs
logs/
logs/access.log
logs/app.log
logs/error.log
rohit@Rohit-PC:~/grinding/linux-day1/app$ ls
config  data  logs
rohit@Rohit-PC:~/grinding/linux-day1/app$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ ls
app  backup  tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd backup
rohit@Rohit-PC:~/grinding/linux-day1/backup$ ls
backup.tar
rohit@Rohit-PC:~/grinding/linux-day1/backup$ cd backup.tar
-bash: cd: backup.tar: Not a directory
rohit@Rohit-PC:~/grinding/linux-day1/backup$ cat backup.tar
logs/0000755000175000017500000000000015245737533011074 5ustar  rohitrohitlogs/access.log0000644000175000017500000000000015245737533013026 0ustar  rohitrohitlogs/app.log0000644000175000017500000000000015245737533012345 0ustar  rohitrohitlogs/error.log0000644000175000017500000000000015245737533012716 0ustar  rohitrohitrohit@Rohit-PC:~/grinding/linux-day1/backup$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$ ls
app  backup  tmp
rohit@Rohit-PC:~/grinding/linux-day1$ cd tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ ls
test1.tmp  test2.tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ rm "*.tmp"
rm: cannot remove '*.tmp': No such file or directory
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ ls "*.tmp"
ls: cannot access '*.tmp': No such file or directory
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ rm *.tmp
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ ls
rohit@Rohit-PC:~/grinding/linux-day1/tmp$ cd ..
rohit@Rohit-PC:~/grinding/linux-day1$
```