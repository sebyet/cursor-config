# Add Documentation

Writes documentation files in the `doc/` folder to create a track record of your project. Each type of documentation uses a specific naming convention and is saved in the `doc/` folder.

## Documentation File Structure

All documentation files are written in the `doc/` folder with specific naming:

### File Naming Conventions

1. **Init/Setup:** `init-project-(date).md`
   - Format: `init-project-YYYY-MM-DD.md`
   - Example: `init-project-2024-01-15.md`
   - Used for: Project initialization, setup, configuration

2. **Features:** `feature-name-date.md`
   - Format: `feature-{feature-name}-YYYY-MM-DD.md`
   - Feature name should be lowercase with hyphens (e.g., `contact-form`, `user-authentication`)
   - Example: `feature-contact-form-2024-01-15.md`
   - Used for: New features, feature additions, feature changes

3. **Deployments:** `deploy-feature-date.md`
   - Format: `deploy-{feature-name}-YYYY-MM-DD.md`
   - Feature name should be lowercase with hyphens
   - Example: `deploy-contact-form-2024-01-15.md`
   - Used for: Deployments, releases, going live

## File Location

**All documentation files go in:** `doc/` folder (create it if it doesn't exist)

## Your Job

1. **Create the doc folder if needed**
   - Check if `doc/` folder exists
   - Create it if it doesn't exist
   - Make sure it's in the project root

2. **Determine documentation type**
   - **Init/Setup:** Project initialization, setup, configuration
   - **Feature:** New features, feature additions, feature changes
   - **Deployment:** Deployments, releases, going live

3. **Generate filename**
   - Use current date in YYYY-MM-DD format
   - For features: Extract feature name from context (lowercase, hyphens)
   - For deployments: Extract feature name from context (lowercase, hyphens)
   - Format according to naming conventions above

4. **Write documentation file**
   - Write clear description of what was done
   - Include details: what, why, when, how
   - Add any important notes or decisions
   - Include relevant technical details
   - Save to `doc/{filename}.md`

5. **Document content should include:**
   - **What:** What was done/changed
   - **Why:** Reason for the change
   - **When:** Date and time
   - **How:** Technical implementation details
   - **Impact:** What this affects
   - **Notes:** Any important information

## Integration with Other Commands

These commands automatically use this documentation structure:
- `setup-new-project.md` → Creates `init-project-YYYY-MM-DD.md`
- `add-feature.md` → Creates `feature-{name}-YYYY-MM-DD.md`
- `publish-production.md` → Creates `go-live-production-{feature}-YYYY-MM-DD.md`
- `publish-feature.md` → Creates `preview-{feature}-YYYY-MM-DD.md`
- `database-migration.md` → Creates `doc/feature-database-migration-YYYY-MM-DD.md`

These commands do NOT create documentation automatically:
- `add-error-handling.md`
- `create-pr.md`
- `build-project.md`
- `fix-everything.md`

## What to Tell the User

- Explain you're adding documentation
- Show them the filename that will be created
- Tell them where it's saved (`doc/` folder)
- Make sure the documentation is clear and helpful

## Examples

### Init Documentation
```
File: doc/init-project-2024-01-15.md
Content: Project initialization, tools installed, configuration, etc.
```

### Feature Documentation
```
File: doc/feature-contact-form-2024-01-15.md
Content: Feature description, implementation details, changes made, etc.
```

### Deployment Documentation
```
File: doc/deploy-contact-form-2024-01-15.md
Content: Deployment details, version, URL, what was deployed, etc.
```

## Checklist

- [ ] `doc/` folder exists (created if needed)
- [ ] Documentation type determined (init/feature/deployment)
- [ ] Filename generated with correct format
- [ ] Documentation content written (what, why, when, how, impact, notes)
- [ ] File saved to `doc/{filename}.md`
- [ ] Documentation is clear and helpful!
