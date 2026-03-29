# Recommended Usage Pattern

This guide shows how to use the hub effectively with different LLM tools.

## General Rule

Do not dump the whole hub into context.

Instead:

1. start with `START.md`
2. load core rules and the dynamic rules index
3. detect task scope
4. load only the relevant standards and workflow pages
5. add memory or operations pages only if needed

## Best Fit

This hub works best with tools that can read files on demand.

Examples:

- Codex
- Anti Gravity
- Claude with project files
- ChatGPT with folder upload or connected workspace
- Cursor

## ChatGPT

Recommended pattern:

1. Upload the `Engineering Hub` folder if the workspace supports it.
2. Paste the **Minimal Starter Prompt**.
3. Ask the model to read `START.md` first and list the files it loaded.
4. Give the real task only after the model confirms scope and loaded files.

Good for:

- planning
- implementation help
- review assistance
- summarizing changes

Watch out for:

- over-eager summarization instead of actually reading the files
- forgetting loaded rules in long chats
- context bloat if too many pages are pasted at once

If the chat gets long, ask the model to restate:

- detected scope
- loaded hub files
- current task goal

## Codex

Recommended pattern:

1. Keep the hub in the workspace.
2. Ask Codex to read `START.md` first.
3. Tell it to list loaded files and scope before editing.
4. Let it implement, then ask it to verify the change against the loaded standards.

Good for:

- file-aware implementation
- scoped edits
- review and validation
- maintaining the hub itself

Best practice:

- keep the hub near the repo root or in a clearly named shared folder
- refer to files by path, not by title alone

## Anti Gravity

Recommended pattern:

1. Keep the handbook available inside the workspace or mounted project files.
2. Ask Anti Gravity to read `START.md` first.
3. Require it to report scope, loaded files, and assumptions before making changes.
4. If the task is domain-specific, tell it to check `15 Dynamic Rules/Rules Index.md` for matching rule packs.

Good for:

- file-aware implementation
- repeatable team workflows
- enforcing shared engineering rules

Watch out for:

- starting implementation before confirming which files were loaded
- loading the entire handbook when only a few files are needed
- skipping dynamic rule packs for domain-heavy work

## Claude

Recommended pattern:

1. Add the hub as project knowledge or upload the folder.
2. Paste the **Minimal Starter Prompt**.
3. Ask Claude to read `START.md` and decide which files to load before solving the task.
4. For large tasks, ask it to restate the active rules before coding.

Good for:

- architecture reasoning
- refactor planning
- design tradeoff analysis
- reviewing whether a change respects boundaries

Watch out for:

- confident guesses when structural ambiguity exists
- pulling in too much context if asked to "read everything"

## Suggested Default Workflow

For most coding tasks:

1. Give the model the starter prompt.
2. Ask it to read `START.md`, then core rules and any matching dynamic rule files.
3. Give the actual task.
4. Require it to report detected scope, loaded files, and assumptions.
5. Require a brief review before finalizing.

## What To Avoid

- pasting all files for every task
- mixing the hub with unrelated long docs in the same prompt
- letting the model skip scope detection
- asking for implementation before the model confirms what it loaded
