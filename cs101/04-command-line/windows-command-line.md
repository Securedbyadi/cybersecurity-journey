# Windows Command Line

**Date:** 2026-09-28 · **Block:** CS101 · **Time:** 60 min

## What this covers
Basic cmd commands, grouped the way I noted them: system basics, network, files and directories,
and processes.

## What I did

### Basics
```cmd
set                     :: check the path
ver                     :: version of the OS
systeminfo              :: OS info
driverquery | more      :: more turns a long response into pages
help
cls
```

### Network
```cmd
ipconfig                :: network info (/all for detailed)
ping example.com        :: check if the target server is connected
tracert example.com
nslookup example.com    :: server / host / domain IP address
netstat                 :: current connections
```

`netstat` options:

| Option | Shows |
|---|---|
| `-a` | all active |
| `-h` | help |
| `-b` | program associated |
| `-o` | reveals process ID |
| `-n` | numerical form of addresses and ports |

`netstat -abon` combines them for all the details.

### Files and directories
```cmd
cd                      :: current drive / directory
cd <dir>                :: navigate to target directory
cd ..                   :: move up one step
dir                     :: child directories
dir /a                  :: hidden directories
dir /s                  :: all sub-directories
tree                    :: visual of sub-directories
mkdir <name>            :: make directory
rmdir <name>            :: delete directory
```

### Processes
```cmd
tasklist
taskkill
```
