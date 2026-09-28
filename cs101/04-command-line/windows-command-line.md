# Windows Command Line

**Completed:** 2026-09-28 · **Block:** CS101 · **Sessions:** 1

## What this covers
Basic cmd commands, grouped the way I noted them: system basics, network, files and directories,
and processes.

## What I did

### Basics
```cmd
set                     :: check the path
ver                     :: version of the OS
systeminfo              :: OS info
hostname                :: computer name
whoami                  :: current user
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
type <file>             :: read a text file
copy <src> <dest>       :: duplicate
move <src> <dest>       :: relocate
del <file>              :: delete (erase does the same)
```

### Processes
```cmd
tasklist
tasklist /FI "imagename eq notepad.exe"   :: filter by process name
taskkill /PID <id>      :: end a process
```

### Utilities
```cmd
chkdsk                  :: scan a disk for bad sectors
sfc /scannow            :: scan and repair system files
```

### Power
```cmd
shutdown /s             :: shut down
shutdown /r             :: restart
shutdown /a             :: abort
```

## What I learned
- `netstat -abon` shows each connection with its program and process ID, so a connection can be tied to a process.
- `dir /a` shows hidden items and `dir /s` includes subfolders.
- Piping long output into `more` makes it readable page by page.

## What confused me
- cmd switches use `/` while network tools use `-`; `<command> /?` shows the right form.
- `set` lists every environment variable; `echo %PATH%` shows just the path.

## Where this shows up in a real SOC
Run `netstat -abon` to tie a suspicious connection to a program and PID, then `tasklist` to confirm the process.
