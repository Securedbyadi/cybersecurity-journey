# Windows PowerShell

**Completed:** 2026-10-01 · **Block:** CS101 · **Sessions:** 2

## What this covers
PowerShell is an object-based shell and scripting language built on .NET. This room covers finding commands, working with files, filtering output, system and network checks, and running commands remotely.

## What I did
- Discovery: `Get-Command`, `Get-Help`, `Get-Alias`, `Write-Output` (the cmdlet behind the `echo` alias)
- Files: `Get-ChildItem`, `Set-Location`, `New-Item`, `Remove-Item`, `Get-Content`
- Pipeline: `Where-Object`, `Sort-Object`, `Select-Object`, with comparison operators `-eq`, `-ne`, `-gt`, `-lt`
- System and network: `Get-ComputerInfo`, `Get-NetIPConfiguration`, `Get-LocalUser`
- Live analysis: `Get-Process`, `Get-Service`, `Get-NetTCPConnection` (shows `OwningProcess`), `Get-FileHash`
- Remote: `Invoke-Command` with `-ComputerName` and `-ScriptBlock`

```powershell
Get-Command -Name *Process*
Get-Process | Sort-Object CPU -Descending | Select-Object -First 5
Get-NetTCPConnection | Where-Object State -eq Established
```

## What I learned
- Cmdlets follow Verb-Noun, so `Get-Command` and `Get-Help` find the right one without memorising.
- The pipeline passes objects, not text, so `Where-Object`, `Sort-Object` and `Select-Object` work on properties.
- `Get-NetTCPConnection` exposes the owning process, which is the PowerShell version of `netstat -abon`.

## What confused me
- Comparisons use `-eq` and `-gt`, not `==` and `>`.
- Aliases like `echo` hide the real cmdlet, so `Get-Alias` tells me what a command actually is.

## Where this shows up in a real SOC
Quick host triage: list processes, services, connections and file hashes, and run the same checks on remote machines with `Invoke-Command`.
