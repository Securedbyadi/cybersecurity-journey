# Linux Shells

**Completed:** 2026-10-02 · **Block:** CS101 · **Sessions:** 1

## What this covers
What a shell is, the common Linux shells, and the basics of writing a shell script.

## What I did
- Interaction: `ls`, `grep`
- Shell info: `history`, `echo $SHELL`, `cat /etc/shells`
- Scripting: shebang (`#!/bin/bash`), variables, `for` loops, `if` / `then` / `else`, `chmod +x` to make a script executable
- Practical: edited a script to search `.log` files in a directory for keywords

```bash
echo $SHELL
cat /etc/shells
chmod +x script.sh
./script.sh
```

## What I learned
- The shell is the layer between me and the operating system; Bash is the usual default and others like Fish add extras such as syntax highlighting.
- A script is commands plus a shebang, variables, loops and conditions.
- A script has to be given execute permission with `chmod +x` before it will run.

## What confused me
- Why a script will not run until it has execute permission.
- Bash syntax is whitespace-sensitive, so a missing space can break a condition.

## Where this shows up in a real SOC
Searching many log files for keywords with `grep` or a short loop script instead of opening each file by hand.
