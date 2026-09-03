
## Application Server File Management & Log Backup

### Task Structure :
- Created Files in this structure
```bash
/grinding/linux-day1/
│
├── app/
│   ├── config/
│   │   ├── app.conf
│   │   └── database.conf
│   ├── logs/
│   │   ├── app.log
│   │   ├── error.log
│   │   └── access.log
│   └── data/
│       ├── users.txt
│       └── products.txt
│
├── backup/
│   └── logs-....tar.gz
│
├── tmp/
│
├── backup_logs.sh
│
└── notes.md
```

### Step 1 - Create the environment

- Create the complete directory structure above.
- Then create these files:
```bash
app/config/app.conf
app/config/database.conf

app/logs/app.log
app/logs/error.log
app/logs/access.log

app/data/users.txt
app/data/products.txt

tmp/test1.tmp
tmp/test2.tmp
```
- Put some sample text inside each file.

### Step 2 - Investigate the server

- Using Linux commands, answer these questions:

A. Find all .log files  
Expected:
```bash
app.log
error.log
access.log
```
B. Find all .conf files    
C. Find all .tmp files  
D. Find all files under app/

### Step 3 - Permissions

- The configuration files contain sensitive information.

Set:
```bash
app.conf
database.conf
```
so that:

Owner → read + write    
Group → read    
Others → no permissions

- Then verify the permissions.

### Step 4 - Ownership
- Check the current:
```bash
owner
group
```
- of the files inside app/.

### Step 5 - Archive the logs
- Create an archive containing:
```bash
app.log
error.log
access.log
```
Store the archive inside:
```bash
backup/
```
- Then verify that the archive contains all three files.

### Step 6 - Cleanup
- The tmp/ directory contains temporary files.
- Delete the .tmp files without deleting the tmp directory itself.
- Then verify that tmp/ is empty.