## Process-Service-Management :

### Scenario :
- We are managing a Linux application server.
- The server administrator reports:     
    "The application server is behaving strangely. Check the running processes, investigate resource usage, manage process priority, terminate an unnecessary process, and verify that an important system service is running correctly."

- Our job is to investigate and resolve the situation.

### 1 - Process Investigation :
- Investigate the currently running processes.
- We need to:
    - View processes running in your current session.
    - View processes from all users.
    - Identify processes consuming CPU and memory.
    - Use top to observe the system in real time.
    - Pick one process and inspect its details.

### 2 - Process Priority :
- The server has a background job that should run with lower CPU scheduling priority so important processes get preference.
- We need to:
    - Create a safe test process.
    - Run one process with normal priority.
    - Run another with a higher nice value.
    - Compare their priority values.
    - Verify the difference using your process-monitoring commands.

### 3 - Process Termination :
- One of your test/background processes is no longer required.
- We need to:
    - Identify its PID.
    - Terminate it.
    - Verify that it is no longer running.

### 4 - Service Management :
- Now switch from processes to services.
- The server's SSH service is important because administrators need remote access.
- We need to:
    - Check the current status of the SSH service.
    - Stop the service.
    - Verify that it stopped.
    - Start it again.
    - Verify that it is running.
    - Restart the service.
    - Check its status again.

### 5 - Service Troubleshooting :
- Imagine the service has started but you're seeing an error.
- Our job is to investigate the service logs.
- We need to:
    - Check recent logs for the service.
    - Look for errors/warnings.
    - Determine whether the service is currently healthy.