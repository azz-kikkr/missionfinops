# Publish Gate — mandatory

## Never push without explicit approval

Never run `git push` unless the user explicitly says one of these exact phrases:

- "ship it"
- "push it"
- "deploy it"
- "publish it"

## Default workflow

1. Make draft changes locally
2. Show changed files
3. Show preview path (e.g. `file:///C:/Users/yuvde/Downloads/mit-site/missionfinops-clean/...`)
4. Wait for approval
5. Commit only if approved
6. Push only if explicitly approved with one of the phrases above

Writing, editing, previewing, committing, and pushing are separate steps. Never collapse them.

## Screenshots and sensitive content

Never use uploaded screenshots or account-console screenshots in any committed file unless the user explicitly confirms they are:

1. Scrubbed of PII (account IDs, ARNs, emails, resource names)
2. Approved for publishing

Assume all screenshots contain sensitive data until told otherwise.
