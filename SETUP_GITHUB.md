# Publish This Repository to GitHub

The repository is prepared as a local Git repository with an initial commit. Publish it as a **private** repository first.

## Recommended repository settings

- **Owner:** `mars0127`
- **Repository name:** `gymfinder-canada`
- **Visibility:** Private
- **Description:** `Toronto-first gym discovery and comparison platform focused on exact equipment and verifiable facility data.`
- **Issues:** Enabled
- **Discussions:** Disabled initially
- **Wiki:** Disabled initially
- **License:** None until the founders make a deliberate IP/open-source decision

## Option A — GitHub Desktop

1. Extract the downloaded repository folder.
2. Open GitHub Desktop.
3. Select **File → Add Local Repository**.
4. Choose the extracted `gymfinder-canada` folder.
5. Select **Publish repository**.
6. Use the recommended name and description above.
7. Keep **Keep this code private** selected.
8. Publish the repository.

## Option B — Git command line

First create an empty private repository named `gymfinder-canada` on GitHub. Do **not** initialize it with a README, `.gitignore`, or licence because those files already exist locally.

Then run:

```bash
cd path/to/gymfinder-canada
git remote add origin https://github.com/mars0127/gymfinder-canada.git
git push -u origin main
```

When using GitHub CLI instead:

```bash
gh auth login
gh repo create gymfinder-canada --private --source . --remote origin --push
```

## Invite the second founder

On GitHub:

1. Open the repository.
2. Open **Settings**.
3. Open **Collaborators** or **Collaborators and teams**.
4. Add the partner's exact GitHub username.
5. Ask the partner to accept the invitation.
6. Record both usernames in `docs/COLLABORATION.md` through a small pull request.

## Branch and review setup

Use pull requests immediately, even while the repository is private.

Recommended starting rule:

- Never commit substantial work directly to `main`.
- Use one branch per issue.
- Let the other founder review high-risk changes involving scope, data sources, schema, authentication, authorization, or deployment.
- Do not make mandatory approval rules so strict that both founders become blocked while access and workflows are still being learned. Tighten repository rules after the first few successful pull requests.

## First shared actions

1. Both founders read `docs/PROJECT_BRIEF.md`, `docs/MVP_SCOPE.md`, and `docs/DECISIONS.md`.
2. Open the issues in `docs/INITIAL_BACKLOG.md`.
3. Each founder comments on Issue 1 with any disagreement or missing constraint.
4. Resolve disagreements in the decision log before implementation begins.
5. Do not commit API keys, `.env` files, private participant information, or unlicensed gym images.
