# LLM Write Boundaries

This page defines the default safety boundary for code changes.

## Core Rule

Only modify what the task explicitly requires.

## Usually Allowed

- files directly needed for the requested change
- tests for code you changed
- imports or references broken by your change
- lint or type fixes introduced by your own edits
- small supporting updates required to keep the touched path working

## Ask First

Do not make these changes without explicit approval:

- broad refactors outside the task
- file moves or folder reorganization
- dependency changes
- config or environment changes
- schema or migration changes
- shared contract changes with multi-layer impact
- changes to generated files, fixtures, or seed data

## Never Do Silently

- unrelated cleanup
- opportunistic bug fixes outside scope
- renaming symbols in untouched areas
- changing workflow or standards docs during product work

## If You Find Something Broken Outside Scope

1. Do not fix it silently.
2. Note it in the task summary or project memory.
3. Ask if it blocks the requested work.

## Why This Exists

LLMs tend to over-help. The safest default is precise, traceable change sets.
