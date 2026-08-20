## Processes
- A program currently running is process & every process have unique ID.
- Here process will run in two ways 
    1. Foreground Process
    2. Background Process
- If you enter a command then it will execute then it will become a program then that running program is called process.

### 1. `ps` :
- It is a command & it will shows the executed processes.
- Ex :
```bash
ps      -> Shows processes running under your current terminal
ps -f   -> Shows processes in full format
ps aux  -> Shows processes with detailed info
```
`nice` :
- It contains priority of process
- -20 -- +19 (-20 has high priority where as +19 has low)
- Ex :
```bash
nice -n -19 sleep60s
```
### 2. `top` :
- It is used to monitor running processes & system resources usage in real time.
### 3. `kill` : 
- It is used to send a signal to running processes, usually to stop or terminate it.
```bash
kill -l     --> used to list all available signals
kill PID    --> To kill the process based on program ID
```
## Services 
### `systemctl` :
- It is a Linux command used to manage & check services controlled by systemd.
- Ex :
```bash
systemctl status sshd
systemctl start sshd
systemctl stop sshd
systemctl restart sshd
systemctl enable sshd
systemctl disable sshd
```