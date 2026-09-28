# Windows commands

## cmd

| Command | Does | Example |
|---|---|---|
| `ipconfig` | show network settings | `ipconfig /all` |
| `net user` | list local user accounts | `net user` |
| `net user <name>` | one account's details: group memberships (privileges), last logon | `net user Administrator` |
| `set` | show environment variables, including the path | `set` |
| `ver` | OS version | `ver` |
| `systeminfo` | OS and hardware info | `systeminfo` |
| `more` | page through long output | `driverquery \| more` |
| `help` | list cmd commands | `help` |
| `cls` | clear the screen | `cls` |
| `ping` | check if a host is reachable | `ping example.com` |
| `tracert` | show the route to a host, hop by hop | `tracert example.com` |
| `nslookup` | look up a domain's IP address | `nslookup example.com` |
| `netstat` | current connections (-a all, -b program, -o PID, -n numeric) | `netstat -abon` |
| `cd` | show current directory, or move to another (`cd ..` goes up one) | `cd C:\Users` |
| `dir` | list directory contents (/a hidden, /s sub-directories) | `dir /a` |
| `tree` | visual tree of sub-directories | `tree` |
| `mkdir` | make a directory | `mkdir notes` |
| `rmdir` | delete a directory | `rmdir notes` |
| `tasklist` | list running processes | `tasklist` |
| `taskkill` | end a process by PID or name | `taskkill /PID 1234` |

## Run box (Win + R)

| Command | Opens | Use it for |
|---|---|---|
| `eventvwr.msc` | Event Viewer | reading logs, filtering by event ID, custom views |
| `taskschd.msc` | Task Scheduler | checking existing scheduled tasks, creating new ones |
| `compmgmt.msc` | Computer Management | users and groups, services, event logs in one place |
| `gpedit.msc` | Local Group Policy Editor | Computer Configuration and User Configuration policies |

## PowerShell

| Cmdlet | Does | Example |
|---|---|---|
| `Get-Help` | explain any cmdlet | `Get-Help Get-Process` |
