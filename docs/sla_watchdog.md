# SLA Watchdog (Automation)

## Goal
Automatically detect SLA breaches and overdue deliverables.

## Logic
- If `today > due_date` AND `status != delivered` → SLA breach
- Apply score penalty and raise an exception flag

## Why it matters
Reduces manual tracking and produces consistent, defensible exception reporting.
