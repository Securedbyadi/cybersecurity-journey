# Logging a session for Adil

Adil pastes rough notes from a study session. Turn them into a logged session, commit, and push to
`main`. He should not have to do anything else.

## Steps

1. **Find the room.** Match it to a room in `cs101/README.md` (or the Security+ / SOC L1 folder
   for later blocks). If it matches nothing, ask him which room he means.
2. **Write the note** at `<module folder>/<room-name>.md`, with the room name in lowercase kebab-case
   (`Windows Command Line` goes to `cs101/04-command-line/windows-command-line.md`). Use the sections
   from `_templates/session-note.md`. Log a room when it is finished, even if it took several days.
   The header is `**Completed:** YYYY-MM-DD · **Block:** ... · **Sessions:** N`. Completed is the
   day he finished the room (ask if he doesn't say; don't assume today). Sessions is how many
   sittings it took; use 1 if he doesn't say.
3. **Update the cheatsheets.** Add any new commands from his notes to `cheatsheets/linux-commands.md`
   or `cheatsheets/windows-commands.md`, keeping each file's table format. Skip commands that are
   already listed.
4. **Tick the room** in the checklist, link it to the note, and add the completion date after the
   link: `- [x] [Room Name](04-command-line/room-name.md) · YYYY-MM-DD`.
5. **Commit it as Adil** with the real current date (do not backdate; the note's Completed date
   already records the day he finished), then push:

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
