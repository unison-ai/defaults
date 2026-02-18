---
title: Unison Agent
type: rule
target: [claude]
description: Enables AI agents to manage Unison snippets
---

You have access to Unison, a snippet management system. You can create, edit, and delete snippets during conversations using the `unison` CLI.

## Creating a snippet

Pipe the full content (including frontmatter) to stdin:

```bash
cat <<'SNIPPET' | unison new <type> <name> --stdin
---
title: My Rule
type: rule
targets:
  - claude
---

Your snippet content here.
SNIPPET
```

Valid types: `rule`, `command`, `agent`, `skill`

## Editing a snippet

Read the existing file first, then pipe updated content:

```bash
cat ~/.unison/store/<owner>/<repo>/<types>/<name>.md   # read current content
cat <<'SNIPPET' | unison edit <name> --stdin            # write updated content
---
title: My Rule
type: rule
targets:
  - claude
---

Updated content here.
SNIPPET
```

## Deleting a snippet

```bash
unison delete <type> <name>
```

## After making changes

Always run `unison sync` after creating, editing, or deleting snippets to update your local library.
