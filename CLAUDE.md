# Logging a session for Adil

Adil pastes rough notes from a study session. Turn them into a logged session, commit, and push to
`main`. He should not have to do anything else.

## Steps

1. **Find the room.** Match it to a room in `cs101/README.md` (or the Security+ / SOC L1 folder
   for later blocks). If it matches nothing, ask him which room he means.
2. **Write the note** at `<module folder>/<room-name>.md`, with the room name in lowercase kebab-case
   (`Windows Command Line` goes to `cs101/04-command-line/windows-command-line.md`). Use the sections
   from `_templates/session-note.md`. Date it today unless he gives another date. If he doesn't say
   how long he spent, use 60 min.
3. **Update the cheatsheets.** Add any new commands from his notes to `cheatsheets/linux-commands.md`
   or `cheatsheets/windows-commands.md`, keeping each file's table format. Skip commands that are
   already listed.
4. **Tick the room** in the checklist and link it to the note: `- [x] [Room Name](04-command-line/room-name.md)`.
5. **Commit it as Adil**, so the commit counts on his contribution graph, then push:

   ```bash
   git add -A
   git commit --author="Adil <adilmushtaq088@gmail.com>" -m "CS101: <Room Name>"
   git push origin main
   ```

   Use the block's own prefix for later blocks (`Security+:`, `SOC L1:`). If he logs several rooms
   at once, give each room its own commit.
6. **Reply briefly**, with the note path and anything you had to guess.

## Rules for the note

- **Keep his words.** Fix spelling, grammar, and layout. Don't add facts, definitions, or insights
  that aren't in his notes, and don't pad a section. A five-line note is fine.
- **Keep sections that fit, drop the rest.** If "What confused me" or "Where this shows up in a
  real SOC" is missing, ask him one short question rather than making it up.
- **No flags, room answers, or exam content.** If his notes contain any, leave them out and say so.
- "What I learned" gets three bullets at most.
