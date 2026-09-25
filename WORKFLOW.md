# How I log a session

The last five minutes of every one-hour session.

## Once: get the repo onto my computer

Install Git from [git-scm.com](https://git-scm.com) if it is not there yet, then:

```bash
git clone https://github.com/Securedbyadi/cybersecurity-journey.git
cd cybersecurity-journey
```

## After every room

1. Copy `_templates/session-note.md` into the room's module folder and name it after the room,
   for example `cs101/04-command-line/windows-command-line.md`. Fill it in from memory.
2. Add any new commands to `cheatsheets/linux-commands.md` or `cheatsheets/windows-commands.md`.
3. In `cs101/README.md`, tick the room and turn its name into a link to the note.
4. Commit and push:

```bash
git add .
git commit -m "CS101: <room name>"
git push
```

No terminal nearby: the same steps work in the browser with **Add file → Create new file**.

The commit history is the proof I showed up every weekday, which says more to a hiring manager
than any single note.
