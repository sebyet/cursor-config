# Sync Configuration

Update MCP configuration with your Vercel and Supabase project URLs.

## What This Command Does

- Updates `mcp.json` with your Vercel project URL
- Updates `mcp.json` with your Supabase project URL

## Example Prompts

- "Update MCP config with Vercel URL https://myapp.vercel.app and Supabase URL https://xxxxx.supabase.co"
- "Sync MCP configuration, Vercel: https://project.vercel.app, Supabase: https://abc123.supabase.co"
- "Update mcp.json with my Vercel and Supabase URLs"

## Runbook

1. **Confirm intent**
   - Tell the user you'll update the MCP configuration with their Vercel and Supabase project URLs.
   - Ask for Vercel project URL and Supabase project URL if not provided.

2. **Get URLs from user**
   - Ask for Vercel project URL (e.g., `https://myapp.vercel.app` or project URL from Vercel dashboard)
   - Ask for Supabase project URL (e.g., `https://xxxxx.supabase.co` from Supabase project settings)
   - If URLs are provided in the prompt, use those
   - Validate URLs are in correct format

3. **Update mcp.json**
   - Check that `.cursor/mcp.json` file exists
   - If it doesn't exist, stop and tell the user to run the initial setup first
   - Read the `mcp.json` file
   - Update the Vercel section with the provided project URL
   - Update the Supabase section with the provided project URL
   - Preserve all existing MCP configurations (tokens, credentials, other settings)
   - Only update the URL fields, don't overwrite tokens or other credentials
   - Write the updated JSON back to the file

## What to Tell the User

- **When starting:** "I'll update your MCP configuration with your Vercel and Supabase project URLs."
- **When asking for URLs:** "I need your Vercel project URL and Supabase project URL to update the MCP configuration. Can you provide them?"
- **During execution:** "Updating `mcp.json` with your Vercel and Supabase URLs…"
- **On success:** "Successfully updated `mcp.json` with your Vercel and Supabase project URLs!"
- **If URLs are invalid:** "The URLs you provided don't seem to be in the correct format. Please check your Vercel and Supabase project URLs."
