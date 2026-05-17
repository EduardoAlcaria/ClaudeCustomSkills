Save a quick note to the life vault at C:\Users\Eduardo Alcaria\Documents\life. Follow these steps exactly:

1. Parse the user's input (the $ARGUMENTS after /note) for:
   - The note content
   - Sector or context (if mentioned — work, startup, life, projects, studies, financial, daily)
   - Whether it's a fleeting thought vs. something that deserves its own note

2. Decide where to save:
   - "daily" or no clear sector → append to today's daily note at `00 - System/Daily Notes/YYYY-MM-DD.md`
   - work / startup → create note in `01 - Work/Startup/` or `01 - Work/Job/`
   - life → create note in `02 - Life/`
   - projects → create note in `03 - Projects/`
   - studies → create note in `04 - Studies/`
   - financial → create note in `05 - Financial/`

3. If appending to today's daily note:
   - Read the file first
   - Append the note under a `## Quick Notes` section (create that section at the bottom if it doesn't exist)
   - Format: `- HH:MM — [note content]` (use current time)

4. If creating a new note:
   - Use a short descriptive filename: `YYYY-MM-DD - [topic].md`
   - Frontmatter: sector, status: active, date
   - Content: the note text under `## Notes`
   - Add backlink to sector hub at the bottom

5. Confirm: "Note saved → [file path]" — one line, nothing else.

Do not explain what you are doing. Just parse, save, confirm.
