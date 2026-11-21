# Agents

<!-- https://agents.md -->

## GitHub Actions Workflows

- Always use the latest version
- YML files should begin with --- on the first line.
- All GitHub Actions should use SHA-1 pinned versions.
- All should be formatted with Prettier.
- If using `actions/checkout`, it should have `persist-credentials: false` set.

## .npmrc

- should specify `min-release-age = 1`
- should specify `package-lock = false`

## Git / Pull Requests

- Always use meaningful branch names. Never use random or auto-generated names (e.g. claude/nifty-bardeen-ysr7xa).
- Always squash each PR to a single commit. When you push follow-up changes to an open PR (review or CI fixes), fold them into that commit and use the `git push --force-with-lease` command instead of adding new commits.
