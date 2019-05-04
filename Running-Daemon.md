## 💡 Commands
### ⭕️ Linux
**1. Start**
```
./run_hlstats start
```

**2. Stop**
```
./run_hlstats stop
```

**3. Restart**
```
./run_hlstats restart
```

**4. Status**
```
./run_hlstats status
```

***

### ⭕️ Windows

**1. Start**

```
perl hlstats.pl
If daemon is running as a service, start the service.
```

**2. Stop**

```
Close the console window OR CTRL+C. 
If daemon is running as a service, stop the service.
```

**3. Restart**

```
Stop & Start - more info above 2. Stop, 1. Start
If daemon is running as a service, restart the service.
```

**4. Status**

```
If the console window is visible, it's running :D
If daemon is running as a service, check if service is running.
```



## ⌚️ CRON / Service

### ⭕️ Linux
Use CRON for auto restart daemon, generate awards & clenup.
```
# Check if daemon running (every 30 minutes)
*/30 * * * * cd <your_daemon_directory> && ./run_hlstats start >/dev/null 2>&1

# Auto restart daemon (midnight)
0 0 * * * cd <your_daemon_directory> && ./run_hlstats restart >/dev/null 2>&1

# Generate awards and cleanup
0 0 * * * cd <your_daemon_directory> && ./hlstats-awards.pl >/dev/null 2>&1

# Auto remove old Daemon logs (14 days)
0 0 * * * find <your_daemon_directory>/logs -type f -mtime +14 -exec rm -rf {} \ >/dev/null 2>&1
```

### ⭕️ Windows
Use eg. `NSSM, FireDaemon` to run Daemon as service (check if the daemon is running, auto restart).

Use `Windows Task Scheduler` for generate awards & clenup. 

## 📃 Logs