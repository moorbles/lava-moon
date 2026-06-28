# Contributing

How insights get captured and committed. The point of this file is the extraction ritual. Run it and the repo maintains itself.

## The extraction ritual

At the end of any working session that produced durable insight, paste this into the same chat:

> Review this conversation and extract any durable insights worth keeping. A durable insight is something still true and useful in three months: a customer truth, a positioning angle, a creative hook, a decision and its reasoning, or a buyer objection and its answer. Ignore anything transient. For each one, write a file in the brand-os schema (frontmatter plus body), put it in the right domain folder under brands/noomanara, and name it YYYY-MM-DD-slug.md. Set status honestly: hypothesis unless there is real evidence. If it contradicts a source doc, add a Drift flag. Then commit the new files to the repo under my identity. List what you extracted and what you skipped.

Claude does the transcription you would otherwise forget. You review the list and the status calls.

## Backfill

- Exhaustive. Export full chat history from claude.ai settings, Account, Data. Hand the export to Claude in one session and have it process the JSON into schema files. Only way to get genuinely everything.
- Incremental. Ask Claude to search past Noomanara chats in batches and extract retroactively. Faster, coverage is keyword-driven and imperfect.

## Domains

| Folder | Holds |
|---|---|
| crm | retention, churn, lifecycle, onboarding, subscription, email |
| audience | segments, language mining, pre-purchase truths |
| creative | hooks, angles, naming, comparison assets |
| product | formulation, dosing, format, quality bars |
| supply | sourcing, MOQ, COAs, manufacturer assessment |
| regulatory | Novel Food, claims law, Meta policy, ASA |
| finance | unit-economics learnings, model assumptions |
| legal | SHA, equity, vesting, partnership |
| decisions | locked cross-domain calls and reasoning |

If an insight spans domains, file it where the action lives and cross-link the rest by id.

## Schema field definitions

| Field | Meaning |
|---|---|
| id | Stable handle for cross-referencing. Domain prefix plus number. CRM-001, FIN-003. |
| type | positioning, customer, creative-hook, decision, objection. |
| brand | noomanara for now. The field that makes the repo multi-brand. |
| segment | exhausted-professional, perimenopause-processor, performance-male, anxious-functional, or all. |
| source | Where it came from. Chat name and date, or document name. |
| status | hypothesis, validated, locked. |
| confidence | high, medium, low. |
| author | matt or isabel. |
| created | Extraction date. |
| tags | Free list for retrieval. |

## Dual-identity setup, so both founders commit cleanly

The repo lives on GitHub. Access is governed by GitHub, not Claude.

1. Create the repo private on GitHub. A small org is cleaner long term than a personal account, because it keeps the OS asset org-owned and survives either person leaving.
2. Add the other founder as a collaborator with write access.
3. Each founder connects GitHub to their own Claude account. This is the GitHub MCP custom connector under Settings, Connectors, not the read-only "Add from GitHub" file picker. Requires a paid plan. Pro and Max both qualify.
4. Each authenticates as themselves, so commits attribute correctly. Set `author:` in frontmatter to match.

### Access paths

- "Add from GitHub" file picker. Read only. Good for pulling context into a session. Cannot write.
- GitHub MCP custom connector. Read and write through the API, including creating or updating multiple files as a single commit. This is the write path the extraction ritual uses. Appending markdown is well inside what it does reliably.
- Claude Code or desktop with filesystem. Full git workflow. Available if either of you wants branches and pull requests. Overkill for text files.

### Getting the files onto GitHub the first time, no terminal

1. github.com, sign in, New repository, name it `brand-os`, Private, Create.
2. On the empty repo page, click "uploading an existing file".
3. Unzip the download. Open the inner `brand-os` folder. Select the contents (README, CONTRIBUTING, brands, os-patterns, templates), not the outer folder. Drag those in.
4. Check the file tree preview shows the folders before committing. If subfolders vanished, stop and use GitHub Desktop instead, which mirrors a folder exactly with no drag-and-drop guessing.

### Limits

- Connector actions are conversation-only. Nothing fires on its own. Each capture happens in a session one of you runs.
- Pro has tighter context than Max. On Pro, pull specific files rather than syncing the whole repo as it grows.

## Commit convention

```
add: CRM-001 60-day product promise
add: REG-002 claims spine magnesium conflict
update: FIN-005 status hypothesis -> validated
```
