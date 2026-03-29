# Minimal Starter Prompt

Use this prompt when starting a session with an LLM that can read files.

```text
Read `Engineering Hub/START.md` first and follow it before doing the task.
Do not load the entire handbook unless `START.md` tells you to.

Before starting:
- report detected scope
- report which handbook files you loaded
- report assumptions that could affect correctness
```

## Paste-Only Fallback

If the model cannot read local files, paste:

1. this prompt
2. `START.md`
3. the core-rules files
4. `15 Dynamic Rules/Rules Index.md`
5. `15 Dynamic Rules/Active Rules.md`
6. only the standards and workflow pages needed for the task
