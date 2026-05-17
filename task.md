Create a Todoist task from what the user describes. Follow these steps exactly:

1. Parse the user's input (the $ARGUMENTS after /task) for:
   - Task name/description
   - Due date (if mentioned — "tomorrow", "Friday", "next week", etc.)
   - Priority (if mentioned — "urgent", "important", etc. → p1/p2/p3)
   - Sector (if mentioned — work, startup, job, life, projects, studies, financial)

2. If the sector is NOT clear from the input, ask ONE question:
   "Which sector? Work (Startup / Job) · Life · Projects · Studies · Financial"

3. Map sector to Todoist project:
   - startup → project "Work", section "Startup"
   - job → project "Work", section "Job"  
   - work (generic) → project "Work"
   - life → project "Life"
   - projects → project "Projects"
   - studies → project "Studies"
   - financial → project "Financial"

4. Create the task using the mcp__claude_ai_Todoist__add-tasks tool with:
   - content: the task name
   - projectId or projectName matching the sector
   - dueString if a date was mentioned
   - priority: p1 (urgent), p2 (important), p3 (normal), p4 (default/low)

5. Confirm: "Task created: [task name] → [Sector]" — one line, nothing else.

Do not explain what you are doing. Just parse, optionally ask for sector, create, confirm.
