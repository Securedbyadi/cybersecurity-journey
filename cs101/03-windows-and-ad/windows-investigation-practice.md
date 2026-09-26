# Windows Investigation (practice)

**Date:** 2026-09-25 · **Block:** CS101 · **Time:** ~4 hours

## What this covers
A practice room for Windows: investigating a machine after an attack that happened back in 2019.
Fifteen questions, all practical. It was a hands-on lab built on a real scenario, with no
definitions or multiple-choice questions.

## What I did
Worked through investigation tasks using Event Viewer, Task Scheduler, and the `net` command.
From the logs, scheduled tasks, and user accounts I found:

- which script the attacker used
- which tool was used for passwords
- when the script first ran
- which account was affected
- which site was used for DNS poisoning

```cmd
net user <name>
```

I used this to check a user's privileges and last logon. I opened the tools from the Run box
(`eventvwr.msc`, `taskschd.msc`, `compmgmt.msc`).

## What I learned
- How to analyse logs in Event Viewer: creating custom log views, and finding abnormal activity
  in processes using event log IDs.
- How to schedule tasks and check tasks that already exist in Task Scheduler.
- How to navigate to the right tool for the situation in front of me.

## What confused me
Where to start, and which tool to open for each situation. I got help from Claude in Chrome with
the right navigation paths and which method to follow for each task.
