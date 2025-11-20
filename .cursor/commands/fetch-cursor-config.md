# Fetch Cursor Config

Fetch the `.cursor` directory from a GitHub repository and copy it into this project so everyone stays in sync on commands, rules, and reviews.

## What This Command Does

- Clones the specified repository into `/tmp/cursor-config-temp` using `git clone --depth=1`
- Copies the repo’s `.cursor` directory (commands, rules, reviews) into this project’s `.cursor` directory, preserving structure and overwriting existing files
- Cleans up the temporary clone and verifies the copy succeeded

## Example Prompts

- "Fetch cursor config from https://github.com/sebyet/cursor-config"
- "Get the .cursor directory from https://github.com/username/repo"
- "Update cursor config from GitHub"
- "Sync cursor configuration from https://github.com/myorg/cursor-rules"

## Runbook

1. **Confirm intent**
   - Tell the user you’ll fetch the `.cursor` directory from the repository they provide and copy it into the project.
   - Mention this will update their Cursor configuration with the repository’s latest files.
2. **Clone repository**
   - `git clone --depth=1 <repo-url> /tmp/cursor-config-temp`
   - If cloning fails, explain the likely causes (bad URL, private repo, network issue).
3. **Validate `.cursor` exists**
   - Ensure `/tmp/cursor-config-temp/.cursor` exists.
   - If missing, stop and tell the user the repo doesn’t contain a `.cursor` directory.
4. **Copy configuration**
   - `cp -R /tmp/cursor-config-temp/.cursor/. /Users/sebastien.payet/Projects/sebastien/.cursor/` (or use `rsync -a` if available).
   - Preserve directory structure and permissions.
5. **Clean up**
   - Remove `/tmp/cursor-config-temp`.
6. **Verify and report**
   - Confirm `commands/`, `rules/`, and `reviews/` now reflect the fetched files.
   - Tell the user the Cursor configuration is updated and ready to use.

## What to Tell the User

- **When starting:** “I’ll fetch the `.cursor` directory from the GitHub repository and copy it here so your Cursor configuration matches the repository.”
- **During execution:** “Cloning the repository… Copying `.cursor` directory contents… Cleaning up temporary files…”
- **On success:** “Successfully fetched and copied the `.cursor` directory! Your Cursor configuration now includes the updated `commands/`, `rules/`, and `reviews/`.”
- **If cloning fails:** “The repository URL doesn’t seem accessible. Please check the URL, repo visibility, and your network connection.”
- **If `.cursor` is missing:** “The repository doesn’t contain a `.cursor` directory. Please add it and try again.”

## Technical Notes

- Use `git clone --depth=1` to minimize download time.
- Prefer `rsync -a` to preserve permissions; `cp -R` works if `rsync` is unavailable.
- Guard against partial copies by validating before overwriting.

## See Also

- **[Setup](setup-new-project.md)**: Initial project setup
- **[How to Start](how-to-start.md)**: Learn how to use commands

