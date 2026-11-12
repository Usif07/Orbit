# Contributing to Orbit

## Branches

- `main` is the shared, stable branch. Do not push directly to it.
- Create short-lived branches from the latest `main`, using `feature/<short-name>`, `fix/<short-name>`, or `docs/<short-name>`.
- Keep each pull request focused and small enough to review comfortably.

## Pull requests

1. Open a pull request targeting `main`.
2. Describe the change, how to review it, and any follow-up work.
3. Request at least one teammate review.
4. Address review comments and ensure the required checks pass.
5. Use squash merge, then delete the branch.

## Commits

Use a short conventional prefix where practical, for example `feat: add shipment form`, `fix: validate phone number`, or `docs: describe branch workflow`.

## GitHub repository settings

When the remote repository is created, protect `main` by requiring pull requests, at least one approval, and passing CI checks before merge. Disable force pushes and branch deletion for `main`. These controls must be enabled in GitHub settings; files in this repository cannot enforce them by themselves.
