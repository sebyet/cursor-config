# Update Cursor Config

Fetches the latest `.cursor` folder from the reference repository (`https://github.com/sebyet/cursor-config`) and updates your local `.cursor` configuration with the latest version.

## What This Command Does

1. **Fetches the latest config**
   - Clones or fetches the reference repository temporarily
   - Extracts the `.cursor` folder from the repository
   - Copies it to your current project

2. **Updates your local config**
   - Replaces your local `.cursor` folder with the latest version
   - Preserves any local customizations if needed (with backup)
   - Ensures you have the latest commands, rules, and configurations

3. **Cleans up**
   - Removes temporary files and directories
   - Verifies the update was successful

## Example Prompts

- "Update my Cursor config to the latest version"
- "Sync my .cursor folder with the latest from the repo"
- "Update cursor config from https://github.com/sebyet/cursor-config"
- "Get the latest Cursor configuration"

## Runbook

### 1. Check Prerequisites

**Verify git is available:**
```bash
# Check if git is installed
git --version
```

**What to look for:**
- Git should be installed and accessible
- If not available, inform the user they need to install git

### 2. Create Backup (Optional but Recommended)

**Backup current .cursor folder:**
```bash
# Create a backup of the current .cursor folder
# Use timestamp to avoid conflicts
BACKUP_DIR=".cursor.backup.$(date +%Y%m%d_%H%M%S)"
cp -r .cursor "$BACKUP_DIR" 2>/dev/null || true
```

**What this does:**
- Creates a timestamped backup of your current `.cursor` folder
- Allows you to restore if something goes wrong
- Only creates backup if `.cursor` exists

### 3. Fetch Latest Config from Repository

**Clone repository to temporary location:**
```bash
# Create temporary directory
TEMP_DIR=$(mktemp -d)

# Clone the repository
git clone --depth 1 https://github.com/sebyet/cursor-config.git "$TEMP_DIR"

# Verify .cursor folder exists in the cloned repo
if [ ! -d "$TEMP_DIR/.cursor" ]; then
  echo "Error: .cursor folder not found in repository"
  rm -rf "$TEMP_DIR"
  exit 1
fi
```

**What this does:**
- Creates a temporary directory for the clone
- Uses `--depth 1` to only fetch the latest commit (faster)
- Verifies the `.cursor` folder exists before proceeding

### 4. Copy .cursor Folder to Current Project

**Replace local .cursor with the fetched version:**
```bash
# Remove existing .cursor folder (if it exists)
rm -rf .cursor

# Copy the .cursor folder from the cloned repo
cp -r "$TEMP_DIR/.cursor" .

# Verify the copy was successful
if [ ! -d ".cursor" ]; then
  echo "Error: Failed to copy .cursor folder"
  rm -rf "$TEMP_DIR"
  exit 1
fi
```

**What this does:**
- Removes the existing `.cursor` folder
- Copies the fresh `.cursor` folder from the repository
- Verifies the copy operation succeeded

### 5. Clean Up Temporary Files

**Remove temporary directory:**
```bash
# Clean up the temporary clone
rm -rf "$TEMP_DIR"
```

**What this does:**
- Removes the temporary repository clone
- Frees up disk space
- Keeps the workspace clean

### 6. Verify Update

**Check that the update was successful:**
```bash
# List the contents of .cursor to verify
ls -la .cursor/

# Check git status to see what changed
git status .cursor/
```

**What to look for:**
- `.cursor` folder should exist and contain files
- Git status should show the updated files
- No errors during the process

## What to Tell the User

**When starting:**
- "I'll fetch the latest Cursor configuration from the repository and update your local `.cursor` folder."
- "This will replace your current `.cursor` folder with the latest version from https://github.com/sebyet/cursor-config"

**Before proceeding:**
- "⚠️ **Note:** This will replace your current `.cursor` folder. I'll create a backup first."
- "Fetching the latest configuration from the repository..."

**During execution:**
- "Creating backup of your current `.cursor` folder..."
- "Cloning the latest configuration from the repository..."
- "Copying the updated `.cursor` folder to your project..."
- "Cleaning up temporary files..."

**After completion:**
- "✅ Successfully updated your Cursor configuration!"
- "Your `.cursor` folder has been updated with the latest version."
- "A backup of your previous configuration is available at `.cursor.backup.[timestamp]` if you need it."

**If something goes wrong:**
- "❌ Error: [specific error message]"
- "The update failed. Your original `.cursor` folder should still be intact."
- "If a backup was created, you can restore it from `.cursor.backup.[timestamp]`"

**If git is not available:**
- "Git is required to fetch the configuration. Please install git first."
- "You can install git from https://git-scm.com/downloads"

## Important Notes

- **Backup created:** A backup of your current `.cursor` folder will be created before updating
- **Replaces entire folder:** This replaces your entire `.cursor` folder, not just individual files
- **Requires git:** This command requires git to be installed on your system
- **Network required:** You need an internet connection to fetch from the repository
- **Temporary files:** Temporary files are automatically cleaned up after the operation
- **Safe operation:** Your original configuration is backed up before any changes are made
- **Repository:** Uses `https://github.com/sebyet/cursor-config` as the source

## When to Use This Command

- You want to get the latest Cursor commands and rules
- Your configuration is out of date
- You want to sync with the latest best practices
- You've made changes and want to reset to the official version
- You're setting up Cursor config on a new project

## When NOT to Use This Command

- You have important local customizations you want to keep (merge manually instead)
- You're in the middle of important work (commit your changes first)
- You don't have internet access
- You want to keep specific local modifications

## Alternative: Manual Update

If you prefer to update manually:

```bash
# Clone the repository
git clone --depth 1 https://github.com/sebyet/cursor-config.git /tmp/cursor-config

# Backup your current config
cp -r .cursor .cursor.backup

# Copy the new config
cp -r /tmp/cursor-config/.cursor .

# Clean up
rm -rf /tmp/cursor-config
```

