## System logs
- System logs are records that linux keep track of what happening on system
- Logs are stores in /var
Whenever something breaks in production the Linux System Administrator checks the logs.
- Common logs   
    1. sys log / msg -> System events (helps us to analize system errors)
    2. auth.log / secure -> login & sudo activity (helps to analyze unautorized IP)
    3. kern.log -> kernal issues

### `journalctl` :
- It is a command to view, search, analyze system logs collected by systemd's journal
- Arguments :   
    - -e -> Shows latest logs
    - -f -> Shows live logs
    - -u -> Shows logs for specific system.d unit / service (sshd / nginx)
    - -p -> Filter logs by priority

- Ex :
```bash
journalctl -e
journalctl -f
journalctl -u sshd --> show me the logs of sshd
journalctl -p err --> show me error
```