# Accessibility Audit

Checks your website for accessibility problems so everyone can use it, including people with disabilities. Finds issues with keyboard navigation, screen readers, color contrast, and more.

1. **Check for accessibility issues**
   - Check keyboard navigation (can users navigate without mouse?)
   - Check screen reader support (are elements properly labeled?)
   - Check color contrast (is text readable?)
   - Check touch targets (are buttons big enough?)
   - Check ARIA labels and roles
   - Check form labels and error messages
   - Check focus indicators
   - Tell the user what you found

2. **Fix accessibility problems**
   - Add missing ARIA labels
   - Fix keyboard navigation
   - Improve color contrast
   - Make touch targets larger (≥44px)
   - Add proper form labels
   - Fix focus indicators
   - Ensure semantic HTML

3. **Verify accessibility**
   - Test keyboard navigation
   - Check screen reader compatibility
   - Verify color contrast meets WCAG standards
   - Confirm all issues are fixed

4. **Document accessibility audit**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/accessibility-audit-YYYY-MM-DD.md`
   - Document: issues found, fixes applied, accessibility status

## What to Tell the User

- Explain you're checking for accessibility problems
- List what you're checking (e.g., "Checking keyboard navigation, screen reader support, and color contrast...")
- If you find problems, explain them clearly and fix them
- Show progress of each check
- Tell them when accessibility checks pass
- Document all checks and fixes for the project history

## See Also

- **[Design](../engineer/design.md)**: Advanced design command
- **[Build](../build.md)**: Build accessible features
- **[Test](../test.md)**: Test accessibility
- **[Test Accessibility](../qa/test-accessibility.md)**: Comprehensive accessibility testing
- **[Deploy](../deploy.md)**: Deploy accessible features