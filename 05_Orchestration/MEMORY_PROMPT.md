## Project Parameters
- **Project Name**: {{PROJECT_NAME}}
- **Tech Stack**: {{TECH_STACK}}
- **Core Objective**: {{CORE_OBJECTIVE}}

---

# Memory Prompt

## Instructions

Write a memory document to `{{SESSION_MEMORY_PATH}}` for context handoff. This file will be your ONLY context when resuming work.

### If `{{SESSION_MEMORY_PATH}}` Already Exists
1. Read it first
2. Preserve still-relevant sections
3. Mark updated sections with `[UPDATED: YYYY-MM-DD]`
4. Move obsolete content to "## Archive" section at bottom
5. Delete archive entries older than 2 weeks

---

## Required Sections

Line budgets (approximate, ~500 total):
- Sections 1-2: ~30 lines
- Section 3: ~50 lines
- Sections 4-5: ~40 lines
- Section 6: ~150 lines (prioritize this - most valuable)
- Sections 7-8: ~50 lines
- Sections 9-12: ~80 lines
- Buffer: ~100 lines

---

### 1. Project Overview (~10 lines)
What is this codebase? Tech stack? Absolute path to project root: `{{PROJECT_ROOT}}`

### 2. Architecture (~20 lines)
- Key directories with purpose
- Entry points: `{{ENTRY_POINTS}}`
- Data flow between components

### 3. Completed Work (~50 lines, table format)
| Feature | Files Modified | Key Details |
|---------|----------------|-------------|
| Example | `path/to/file.py` | Brief description |

### 4. In-Progress/Blocked (~20 lines)
What's partially done? What's blocking?
- Include error messages if relevant
- Note which file/line you stopped at

### 5. Pending Work (~20 lines, prioritized)
What remains? Reference ticket files if they exist.

### 6. Critical Knowledge (~150 lines)
Non-obvious discoveries that save re-investigation. Use severity markers:

**Severity Levels:**
- 🔴 **CRITICAL**: Will cause failures if forgotten
- 🟡 **IMPORTANT**: Saves significant time  
- 🟢 **HELPFUL**: Nice to know

**Categories:**
- **Gotchas**: Edge cases, things that look wrong but are correct
- **External Services**: API quirks, auth flows, data format surprises
- **Patterns**: What worked vs. what didn't (and why)
- **Data Relationships**: How IDs/keys connect across systems

### 7. Test Data (~30 lines)
Include timestamps - test data expires!

### 8. Quick Start (~20 lines)
Exact commands to run from project root:
{{QUICK_START_COMMANDS}}

### 9. Git State (~15 lines)
Current branch, last commit, uncommitted changes.

### 10. Related Memory Files (~15 lines)
Link to other context files.

### 11. Resume Instructions (~25 lines)
First actions for next session:
```
1. READ FIRST:
   - <specific file to load for context>
2. VERIFY STATE:
   - <command to check status>
3. CONTINUE FROM:
   - Task: <specific next task>
```

### 12. User Preferences (~25 lines)
Patterns established in this session:
- Commits: [Convention]
- Testing: [Preference]
- Style: {{LINTING_RULES}}

---

## What NOT to Include
- Standard library/framework behavior
- Code patterns obvious from reading the file
- Full file contents
- Credentials, secrets, or PII

---

## Self-Verification Checklist
- [ ] Can I restart with only Quick Start commands?
- [ ] Are absolute paths present?
- [ ] Are blocking issues actionable?
- [ ] Did I capture the ONE thing that would waste the most time if forgotten?

---

## Archive
[Move obsolete sections here with date. Delete after 2 weeks.]
