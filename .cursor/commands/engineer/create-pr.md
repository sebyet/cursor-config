# Create Pull Request

Creates a pull request (PR) on GitHub so you can review your changes before merging them. Makes it easy to share your work and get feedback before going live.

1. **Check if ready for PR**
   - Check if code is saved to Git (all changes committed)
   - Check if branch is pushed to GitHub
   - Check if project builds successfully
   - Check if tests pass (if tests exist)
   - Tell the user what you found

2. **Fix issues if needed**
   - **If code not saved:** Commit changes to Git first
   - **If branch not pushed:** Push branch to GitHub
   - **If build fails:** Use `build-project.md` approach - fix build issues
   - **If tests fail:** Use `run-tests.md` approach - fix test failures
   - Don't create PR until everything is ready

3. **Create pull request**
   - Use GitHub CLI (`gh`) to create PR
   - Create PR from current branch to main/master
   - Add descriptive title and description
   - Link PR to related issues if applicable
   - Show PR URL to user

4. **Verify PR created**
   - Check that PR was created successfully
   - Show PR URL and details
   - Tell user they can review and merge it

5. **Document PR creation**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/pr-created-YYYY-MM-DD.md`
   - Document: PR details, branch, changes, PR URL

## What to Tell the User

- Explain you're creating a pull request for their changes
- Check if everything is ready (code saved, pushed, builds, tests pass)
- Fix any issues before creating PR
- Create PR using GitHub CLI
- Show them the PR URL
- Tell them they can review and merge it on GitHub
- Document PR creation

## See Also

### Workflow
- **[Build](../build.md)**: Build features before creating PR
- **[Test](../test.md)**: Test before creating PR
- **[Deploy](../deploy.md)**: Deploy after PR is merged
- **[Publish Production](publish-production.md)**: Deploy to production after PR merge

### Quality Checks
- **[Run Tests](run-tests.md)**: Run tests before creating PR
- **[Build Project](build-project.md)**: Build project before creating PR
- **[Code Review](code-review.md)**: Review code before PR

### Git
- **[Git Workflow](.cursor/rules/git-workflow.mdc)**: Git workflow and PR best practices

