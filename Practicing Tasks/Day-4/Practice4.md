## Shell Scripting :
- Created a small automation script of server health
```bash
#!/usr/bin/bash

# Server Health Check
hostnamectl
date
whoami

# Memory check
df -h
free -h

# Service Check
systemctl status cron

# Conditional logic
if systemctl is-active --quiet cron
then
        echo "Server is Healthy"
else
        echo "WARNING : Server is not running"
fi
```
- then backedup the data into the backup folder
```bash
bash /home/rohit/grinding/linux-day5/server_check.sh >> /home/rohit/grinding/linux-day5/backup/server_info.txt
cat /home/rohit/grinding/linux-day5/backup/server_info.txt
```