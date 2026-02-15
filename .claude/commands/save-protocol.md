---
description: "Finalize and commit the active protocol to git"
---

Find the most recently modified `.md` file in `protocols/`. That's the active protocol.

Read it. Update its **Status** from `Draft` to `Final`.

Then:
1. `git add` the protocol file
2. `git commit` with message format: `"protocol: slug-name"` (e.g., `"protocol: morning-supplement-stack"`)
3. `git push`

Confirm to the user: file path, protocol name, commit done.
