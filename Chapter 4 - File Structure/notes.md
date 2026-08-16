## File Structure :
- In Linux everything is a file

![Linux File System Structure](/images/LinuxFileStructure.jpeg)

### 1. /bin :
- The all commands consists in /bin
- It contains general commands using by normal people
- We can change the command how we want
- First I will navigate to /bin & use this command
``` bash
sudo cp cat Chupinchu
```
- Now chupinchu command have cat feature

### 2. /sbin :
- /sbin also contains commands but these commands can effect system
- in /bin the commands doesn't effect the system
- We can find the commands mainly used for system administration and management
```bash
ip addr
```

### 3. /boot :
- Boot mans simply starting the system
- For starting the system it need some information that info in exists in /boot

### 4. /dev :
- dev stands for device
- Linux represent many hardware devices as files inside /dev
- It used to interact with hardware devices like USB

### 5. /etc :
- /etc contains configuration files

### 6. /mnt :
- If we put CD or Pendrive then system should detect
- Then those files are exists in /mnt (mounting)

### 7. /lib :
- When we run program then we need libraries
- This folder contains those files

### 8. /media :
- It contains media files
- video resolution, full screen etc.

### 9. /opt :
- It is optional directory
- If we are installing third party application the that file will strore in /opt

### 10. /proc :
- Contains process related files

### 11. /sys :
- It contains system related information
- Like how much RAM consume & how much free

### 12. var :
- Contains system logs
- logs means information of what we have done
- Like which file created when, when we login etc.

### 13. /usr :
- It contains information of user

### 14. /tmp :
- It contains temporary files