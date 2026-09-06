## User & Group Access Management

### Scenario :
- We are managing a Linux application server.
- There are three teams:
    - Developers
    - Operations
    - Database
- Each team needs different access to application resources.
Our job is to create the users/groups and configure access correctly.

### 1 - Create Groups :
- Create these groups:
    - developers
    - operations
    - database
### 2 - Create Users :
- Create these users
    - dev1
    - dev2
    - ops1
    - db1
- Assign them to the appropriate groups:

    User --> Group   
    dev1 --> developers  
    dev2 --> developers  
    ops1 --> operations  
    db1 --> database    

- Verify that the users belong to the correct groups.

### 3 - Create Application Structure :
- Inside your Day 2 directory, create
```bash
day-02-user-group-management/
├── application/
│   ├── developers/
│   ├── operations/
│   └── database/
└── shared/

The idea is:

Developers work inside developers/
Operations work inside operations/
Database team works inside database/
Everyone can access shared/
```
### 4 - Configure Ownership :
- Set the appropriate group ownership:

    developers/ → developers    
    operations/ → operations    
    database/   → database  
    shared/     → appropriate shared group  

- Verify using:
```bash
ls -l
```
### 5 - Configure Permissions :
- Our goal
```bash
- Developers :
developers/ should allow:
Developers → read/write/enter
Everyone else → no access

- Operations
operations/ should allow:
Operations → read/write/enter
Everyone else → no access

- Database :
database/ should allow:
Database team → read/write/enter
Everyone else → no access

- Shared :
shared/ should allow all three teams to work with files.
```
### 6 - Test Access :
- Switch between users and test their access.
- For example:
    Can dev1 create a file inside developers/?

    Can dev1 access operations/?

    Can ops1 access developers/?

    Can db1 access database/?

    Can everyone access shared/?

### 7 - Real-World Problem :
- We receive this requirement from your manager:

    "Developers need access to the database team's directory, but they should only be able to read the files. They must not be able to modify or delete anything."

- Configure the permissions to satisfy this requirement.
- Then test it with dev1.