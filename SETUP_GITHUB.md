# GitHub Access and Local Setup

Repository: `https://github.com/mars0127/gymfinder-canada`

## Repository visibility

The accepted decision is to keep the repository private and unlicensed during planning and initial implementation.

Verify in GitHub:

1. Open **Settings → General**.
2. Confirm repository visibility is **Private**.
3. Confirm no public licence has been added.

Changing a previously public repository to private does not undo prior public exposure, so secrets must never be committed regardless of visibility.

## Invite the second founder

1. Open **Settings → Collaborators and teams**.
2. Invite the second founder's GitHub account.
3. Confirm they can clone, create branches, and open pull requests.
4. Update `docs/COLLABORATION.md` with their username.

## Grant the ChatGPT GitHub connection access when repository inspection is desired

A private repository must be included in the GitHub App or connector installation used by ChatGPT. Otherwise repository reads may return `404` even when the URL is correct.

In GitHub, review the installed application's repository access and include `mars0127/gymfinder-canada`. Grant only the minimum access required for the intended workflow.

## Clone with GitHub Desktop

1. Open GitHub Desktop.
2. Select **File → Clone repository**.
3. Choose `mars0127/gymfinder-canada`.
4. Select a local folder.
5. Confirm the current branch and commit before editing.

## Branch and pull-request workflow

1. Create one branch per issue.
2. Do not let two agents edit the same branch simultaneously.
3. Commit coherent changes.
4. Push the branch only when authorized.
5. Open a focused pull request using the repository template.
6. Merge only after acceptance evidence and any required review are complete.

Use `CONTRIBUTING.md` and `docs/AI_AGENT_WORKFLOW.md` for details.

## Local configuration

After application code exists, local secrets will belong in ignored environment files such as `.env.local`. Never commit actual credentials. Commit only safe example files such as `.env.example` with placeholder values.

## Recovery check

Before a consequential agent run, capture:

```bash
git branch --show-current
git rev-parse HEAD
git status --short
```

An unexpected branch, commit, or dirty state should cause a stop rather than an automatic reset, stash, clean, or checkout.
