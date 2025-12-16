# Git Commit & Push

## Overview
Perform Git actions to record, track, and share changes in the feature branch. Ensure commits are **atomic, descriptive, and linked to plan work or tasks**, and push updates to the remote repository for backup, CI/CD, and collaboration.

## Steps
1. **Stage Changes**
   - Add files to staging area:
     - `git add <files>` or `git add .` for all changes
   - Review staged changes:
     - `git status`
     - `git diff --staged` (optional)

2. **Commit Changes**
   - Create a descriptive commit message:
     - Example: `feat(auth): implement login endpoint (#123)`
   - Commit staged changes:
     - `git commit -m "your descriptive message"`

3. **Push Feature Branch**
   - Push to remote repository:
     - `git push origin <feature-branch>`
   - Ensure branch is up-to-date with main before pushing if necessary:
     - `git fetch origin`
     - `git rebase origin/main` or `git merge origin/main`
   - Resolve conflicts locally if they arise
   - Push again after resolving conflicts

4. **Verify Remote Branch**
   - Check that the feature branch is visible on remote
   - Ensure CI/CD pipelines are triggered

## Checklist
- [ ] All changes staged for commit
- [ ] Commit message is clear, descriptive, and references plan work or ticket
- [ ] Feature branch pushed to remote
- [ ] Branch up-to-date with main (rebased or merged)
- [ ] Conflicts resolved if any
- [ ] Remote branch verified and CI/CD triggered
