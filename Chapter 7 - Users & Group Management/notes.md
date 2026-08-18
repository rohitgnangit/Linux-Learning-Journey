## Users 
As a system admin you will dealing with users and groups regularly.
There are three types of users and two types of groups.
- **root (UID 0)** : Super user with unlimited privilages
- **System Users (UID 1-999)** : Run services and documents
- **Regular Users (UID 1000+)** : Human users
- **Primary group** : Default group of user, if user created then he will be automatically added into group called "Primary group"
- **Supplimentary group** : Additional groups for access
### Adding User :
- useradd
- Arguments :   
`-g` -> Group   
`-G` -> Subgroup    
`-u` -> UserID  
`-s` -> login shell (/sbin/nologin)
- Ex :
```bash
useradd -g 1000 -m -s /sbin/nologin babu
```
### Modify existing User :
- usermod
- Arguments :   
`-G` -> Supplimentary group   
`-aG` -> add supplimentary group ('a' means append)

### Delete existing user :
- userdel
- Arguments :   
`-r` -> delete user along with home directory   
- **note** : If you use userdel /home/user stays

## Group Management 
- Group info stores in /etc/group

### Create group :
```bash
sudo groupadd -g xxx groupname
```
- Arguments :   
`-g` -> group ID

### Delete group :
```bash
sudo groupdel groupname
```
- **note** : Cannot delete if it is primary group of any user

### Adding user to multiple groups :
```bash
sudo usermod -aG group1,group2,group3 username
```