# Incident & Postmortem Guide

Load this page only for incidents or postmortems.

## Severity

| Level | Meaning |
| --- | --- |
| P0 | outage, data loss, or severe security issue |
| P1 | major user-facing failure |
| P2 | partial degradation with workaround |
| P3 | low-impact issue |

## Incident Template

### INC-[ID] - Short Title

- **Start time:** YYYY-MM-DD HH:MM UTC
- **End time:** YYYY-MM-DD HH:MM UTC or `ongoing`
- **Severity:** `P0` | `P1` | `P2` | `P3`
- **Impact:** who was affected and how
- **Detection source:** alert, report, or internal discovery
- **Mitigation:** rollback, hotfix, feature flag, or `none`
- **Owner:** response lead

## Postmortem Template

Required for every P0 and P1 incident.

### Postmortem: INC-[ID] - Short Title

- **Summary:** what happened and how it ended
- **Root cause:** the actual technical cause
- **Triggering change:** task, PR, deploy, or `unknown`
- **What worked:** useful parts of detection or response
- **What failed:** gaps in code, process, or tooling
- **Corrective actions:** concrete fixes with owners and due dates
- **Preventive actions:** changes that reduce recurrence risk

## Rules

- Keep the write-up factual and blameless.
- Track actions to closure.
- Add a Never-Again rule if the failure pattern is likely to repeat.
