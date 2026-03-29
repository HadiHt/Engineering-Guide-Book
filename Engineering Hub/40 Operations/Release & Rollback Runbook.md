# Release & Rollback Runbook

Load this page only for deployment planning, release execution, or rollback work.

## Pre-Release

- [ ] All intended changes are merged or explicitly listed
- [ ] Validation and required approvals are complete
- [ ] Risky changes such as config, schema, or permission updates were reviewed
- [ ] Rollback conditions are defined
- [ ] The deployment owner and monitoring window are clear

## Release Plan

- **Deployment order:** exact sequence
- **Required config changes:** list or `none`
- **Verification checks:** concrete smoke tests
- **Monitoring checkpoints:** dashboards, alerts, logs

## Rollback Plan

- **Trigger conditions:** what forces rollback
- **Rollback steps:** exact reversal procedure
- **Data handling:** migration or state recovery plan, or `not applicable`
- **Post-rollback checks:** how to confirm recovery

## Post-Release

- [ ] Outcome recorded: `success` | `rolled back` | `partial`
- [ ] Any incidents linked
- [ ] Stable behavior observed during the initial monitoring window
