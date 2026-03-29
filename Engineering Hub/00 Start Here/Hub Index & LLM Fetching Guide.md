# Hub Index & LLM Fetching Guide

Use this page to decide what to load.

Rule: load the smallest set of pages that lets you do the work safely.

## Always Load First

- **AI Agent Instructions** in `10 Core Rules`: execution contract for the session
- **Never-Again Rules** in `10 Core Rules`: recurring mistakes to avoid
- **LLM Write Boundaries** in `10 Core Rules`: what may and may not be changed

## Load By Task Type

### Starting a task

- **Definition of Done** in `30 Workflow`
- **Development Workflow** in `30 Workflow`

### Resuming in-progress work

- **Session Resume Protocol** in `30 Workflow`

### Frontend work

- **React + TypeScript Standards** in `20 Standards`
- **Git Standards** in `20 Standards`
- **PR Review Checklist** in `20 Standards`

### Backend work

- **C# Coding Standards** in `20 Standards`
- **Git Standards** in `20 Standards`
- **PR Review Checklist** in `20 Standards`

### Work that changes architecture or system boundaries

Add:

- **Architecture Rules**
- **Architecture Decisions (ADR)** in `50 Memory` only if a durable design decision should be recorded

### Incident, release, or rollback work

Load only the relevant operational page:

- **Incident & Postmortem Guide**
- **Release & Rollback Runbook** in `40 Operations`

## Pages Usually Not Needed

Skip these unless the task specifically calls for them:

- **Architecture Rules**
- **Architecture Decisions (ADR)**
- **Incident & Postmortem Guide**
- **Release & Rollback Runbook**
- **Engineering Standards** parent page

## Session Caching

Once a standards page has been loaded in the current session, do not reload it unless:

- scope changes
- the user asks for a refresh
- the file changed during the session
- a workflow step explicitly requires a fresh read

## Directory

- `10 Core Rules`: session rules and safety boundaries
- `20 Standards`: frontend, backend, git, review, and architecture standards
- `30 Workflow`: execution flow, review flow, and completion checklist
- `40 Operations`: incident and deployment procedures
- `50 Memory`: optional task log and ADRs
