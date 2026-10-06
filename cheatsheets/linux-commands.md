# Linux commands

| Command | Does | Example |
|---|---|---|
| `pwd` | print working directory | `pwd` |
| `grep` | search text for a keyword | `grep "error" *.log` |
| `history` | list previously run commands | `history` |
| `echo $SHELL` | show the current shell | `echo $SHELL` |
| `cat /etc/shells` | list the shells installed on the system | `cat /etc/shells` |
| `chmod +x <script>` | give a script execute permission | `chmod +x script.sh` |
| `#!/bin/bash` | shebang: first line of a script, says to run it with Bash | `#!/bin/bash` |
| `telnet <ip> <port>` | connect to a service listening on a port | `telnet 10.10.10.10 80` |
| `dhclient` | request an IP address and settings from DHCP | `sudo dhclient` |
| `traceroute <ip>` | show the route to a host, hop by hop | `traceroute 8.8.8.8` |
| `ip route` | show the routing table | `ip route` |
| `ping <ip>` | check if a host is reachable | `ping 8.8.8.8` |
