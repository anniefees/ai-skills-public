---
name: no-secrets-in-git
description: >-
  Use this when committing, opening a PR, or handling API keys, so credentials never end up in git.
status: draft
updated: 2026-11-17
---
# No secrets in git

Credentials never belong in a repository, a commit, a pull request, a gist, or an attachment that looks like an env file.

## Never put in git (or paste into a PR description)
- API keys, tokens, passwords, private keys, session cookies
- `.env`, `.env.*`, credential JSON, PEM/P12 files, `secrets.yaml`
- Screenshots or logs that show a live key value
- Hardcoded `x-api-key`, `Authorization: Bearer ...`, or similar in source

## Do instead
1. Store secrets only in a secret store, keychain, password manager, or host env (for example `YOUR_API_KEY`). Reference the variable's **name**, never the value.
2. Before every commit or PR, scan the diff for key-shaped strings, `.env`, and auth headers. Strip anything sensitive and rotate the key if it may have leaked.
3. Keep `.gitignore` covering at least: `.env`, `.env.*`, `*.pem`, `*.p12`, `*credentials*`, `*secret*`.
4. Docs mention env var names and "ask for the key via a secure field", never sample values.
5. If a secret was committed: stop, remove it from history or rotate it right away, and say so plainly.

## Done when
Secrets are referenced only by name, the ignore list covers credential files, and the diff has no secret values.
