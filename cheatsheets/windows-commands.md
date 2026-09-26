# Windows commands

## cmd

| Command | Does | Example |
|---|---|---|
| `ipconfig` | show network settings | `ipconfig /all` |
| `net user` | list local user accounts | `net user` |
| `net user <name>` | one account's details: group memberships (privileges), last logon | `net user Administrator` |

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
