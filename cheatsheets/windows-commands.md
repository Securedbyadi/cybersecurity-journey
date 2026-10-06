# Windows commands

## cmd

| Command | Does | Example |
|---|---|---|
| `ipconfig` | show network settings | `ipconfig /all` |
| `ipconfig /release` | give up the current DHCP lease | `ipconfig /release` |
| `ipconfig /renew` | request a new DHCP lease | `ipconfig /renew` |
| `net user` | list local user accounts | `net user` |
| `net user <name>` | one account's details: group memberships (privileges), last logon | `net user Administrator` |
| `set` | show environment variables, including the path | `set` |
| `ver` | OS version | `ver` |
| `systeminfo` | OS and hardware info | `systeminfo` |
| `hostname` | computer name | `hostname` |
| `whoami` | current user | `whoami` |
| `more` | page through long output | `driverquery \| more` |
| `help` | list cmd commands | `help` |
| `cls` | clear the screen | `cls` |
| `ping` | check if a host is reachable | `ping example.com` |
| `tracert` | show the route to a host, hop by hop | `tracert example.com` |
| `arp -a` | show cached IP to MAC address mappings | `arp -a` |
| `route print` | show the routing table | `route print` |
| `nslookup` | look up a domain's IP address | `nslookup example.com` |
| `netstat` | current connections (-a all, -b program, -o PID, -n numeric) | `netstat -abon` |
| `cd` | show current directory, or move to another (`cd ..` goes up one) | `cd C:\Users` |
| `dir` | list directory contents (/a hidden, /s sub-directories) | `dir /a` |
| `tree` | visual tree of sub-directories | `tree` |
| `mkdir` | make a directory | `mkdir notes` |
| `rmdir` | delete a directory | `rmdir notes` |
| `type` | read a text file | `type notes.txt` |
| `copy` | duplicate a file | `copy notes.txt backup.txt` |
| `move` | relocate a file | `move notes.txt C:\Temp` |
| `del` / `erase` | delete a file | `del notes.txt` |
| `tasklist` | list running processes (`/FI` filters, e.g. by process name) | `tasklist /FI "imagename eq notepad.exe"` |
| `taskkill` | end a process by PID or name | `taskkill /PID 1234` |
| `chkdsk` | scan a disk for bad sectors | `chkdsk` |
| `sfc /scannow` | scan and repair system files | `sfc /scannow` |
| `shutdown` | /s shut down, /r restart, /a abort | `shutdown /r` |

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
| `Get-Command` | find cmdlets, functions and programs by name | `Get-Command -Name *Process*` |
| `Get-Alias` | show which cmdlet an alias really is | `Get-Alias echo` |
| `Write-Output` | print to the output (the cmdlet behind the `echo` alias) | `Write-Output "hello"` |
| `Get-ChildItem` | list files and folders | `Get-ChildItem C:\Users` |
| `Set-Location` | change directory | `Set-Location C:\Users` |
| `New-Item` | create a file or folder | `New-Item notes.txt` |
| `Remove-Item` | delete a file or folder | `Remove-Item notes.txt` |
| `Get-Content` | read a file's contents | `Get-Content notes.txt` |
| `Where-Object` | filter pipeline output by a condition (`-eq`, `-ne`, `-gt`, `-lt`) | `Get-Process \| Where-Object CPU -gt 100` |
| `Sort-Object` | sort pipeline output by a property | `Get-Process \| Sort-Object CPU -Descending` |
| `Select-Object` | pick properties or the first N objects | `Get-Process \| Select-Object -First 5` |
| `Get-ComputerInfo` | system and OS details | `Get-ComputerInfo` |
| `Get-NetIPConfiguration` | IP configuration of the network interfaces | `Get-NetIPConfiguration` |
| `Get-LocalUser` | list local user accounts | `Get-LocalUser` |
| `Get-Process` | list running processes | `Get-Process` |
| `Get-Service` | list services and their state | `Get-Service` |
| `Get-NetTCPConnection` | current TCP connections, with `OwningProcess` (like `netstat -abon`) | `Get-NetTCPConnection \| Where-Object State -eq Established` |
| `Get-FileHash` | hash of a file | `Get-FileHash .\file.exe` |
| `Invoke-Command` | run a command on a remote computer | `Invoke-Command -ComputerName PC01 -ScriptBlock { Get-Process }` |
