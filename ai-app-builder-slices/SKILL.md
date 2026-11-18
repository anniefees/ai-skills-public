---
name: ai-app-builder-slices
description: >-
  Use this to build or fix a web app with an AI app builder in small, checkpointed, tested slices.
status: draft
updated: 2026-11-17
---
# AI app builder slices

Build or fix a web app with an AI app builder, in small tested slices, with a checkpoint before and after each change.

## Steps
1. If the app is stuck, diagnose read only first and propose a fix. Change nothing until you get a yes.
2. Checkpoint before and after each slice.
3. Keep user and business details out of code; use generic defaults and profile variables.
4. Validate AI output before saving (short fields stay short, no sentences in name fields, keep required footers, fall back to defaults).
5. If the AI service is down, show one calm banner and retry later.
6. Verify with lint, build, and unit tests.
7. Back up a record before editing it, never delete it, and share a preview plus a plain list of changes.

## Rules
- Never put API keys, tokens, or passwords in the code, chat, or commits. See [no-secrets-in-git](../no-secrets-in-git/SKILL.md).
