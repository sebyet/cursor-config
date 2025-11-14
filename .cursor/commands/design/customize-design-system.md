# Customize Design System

Friendly, conversational design system customization for non-technical users. Guides them through visual choices using everyday language, examples, and comparisons—never code or technical jargon. As a design expert, provides professional recommendations and best practices throughout the conversation, explaining why certain choices work well. Updates the design system behind the scenes while keeping the conversation simple and intuitive.

### 1. Read Current Design System (Background Work)

- [ ] Parse `app/globals.css` to extract all design tokens (don't mention this to user)
- [ ] Identify token categories (keep technical names internal)
- [ ] Extract current color values (convert to user-friendly descriptions)
- [ ] Prepare visual comparisons and examples for each category

### 2. Interactive Q&A Session (User-Facing)

**CRITICAL**: Never show technical codes (OKLCH, hex, CSS) to the user. Use:
- Plain English color descriptions
- Visual comparisons ("like the blue in Facebook", "similar to Twitter's buttons")
- Simple choices ("light gray", "bright blue", "warm orange")
- Examples from familiar apps and websites
- Relative descriptions ("darker", "brighter", "more saturated")

**CRITICAL**: As a design expert, provide recommendations alongside questions:
- Share best practices and industry standards
- Explain why certain choices work well
- Offer accessibility considerations (readability, contrast)
- Suggest harmonious color combinations
- Provide UX guidance (what makes interfaces feel professional)
- Be helpful but not pushy—let user make final choice
- Use phrases like "I'd recommend...", "For best results...", "Most apps do...", "A good rule of thumb..."

Engage user conversationally, one category at a time, mixing questions with expert guidance:

#### Base Colors
- [ ] Ask about background with recommendation: "What color should your main background be? Right now it's pure white. You could keep it white, or go with a soft cream, light gray, or even a very pale blue—whatever feels right for your brand. **Recommendation**: I'd suggest a very subtle off-white or light gray rather than pure white—it's easier on the eyes and feels more modern. Pure white can be a bit harsh, especially for long reading sessions."
- [ ] Ask about text color with accessibility guidance: "For text on that background, we currently have almost-black. Would you like to keep it dark, or maybe go with a softer charcoal gray? What feels most readable to you? **Recommendation**: For best readability and accessibility, I'd recommend staying with a very dark color (almost black). It ensures your text meets contrast requirements and is readable for everyone, including users with visual impairments."
- [ ] Ask about cards with UX guidance: "Cards (like these boxes with content) can match the background or be slightly different. What do you prefer? **Recommendation**: Most professional apps use a subtle difference—maybe 2-5% darker or lighter. This creates visual hierarchy without being obvious. Think about Gmail's subtle card backgrounds versus Apple's clean white-on-white—both work, but subtle separation is more common."
- [ ] Ask about dark mode with best practices: "When it's dark, do you want a true black, dark gray, or maybe a deep navy blue? **Recommendation**: I'd suggest avoiding true black—it can create too much contrast and cause eye strain. A dark gray (like #1a1a1a) or deep navy feels more comfortable. Most modern apps use dark gray—think GitHub's dark mode or Twitter's night mode."

#### Primary Colors (Main Brand Color)
- [ ] Ask about brand color with examples: "What's the main color that represents your brand? This is the color for your most important buttons and links. Like how Instagram uses purple, Spotify uses green, or LinkedIn uses blue. What color feels like 'you'?"
- [ ] Provide saturation guidance: "How bright or subtle should it be? Bold and energetic, or calm and professional? **Recommendation**: For most apps, I'd recommend a medium-to-high saturation. Too subtle and buttons won't feel clickable; too bold and it can feel overwhelming. A good rule of thumb: if it's for a consumer app, go bolder. If it's for a professional tool, go slightly more muted."
- [ ] Ask about text on primary with contrast guidance: "When text sits on top of that color, should it be white, black, or something in between? **Recommendation**: White text on colored buttons is the industry standard—it has the best contrast and readability. I'd strongly recommend white unless your primary color is very light."
- [ ] Ask for dark mode with adaptation guidance: "For dark mode, should we use the same primary color or adjust it? **Recommendation**: Most apps slightly brighten the primary color in dark mode so it stands out better against dark backgrounds. I'd suggest keeping the same hue but making it about 10-15% brighter."

#### Secondary Colors
- [ ] Ask about secondary with color theory guidance: "For your secondary buttons and accents, what color works? This should complement your primary color. Some apps use a softer version of the primary, others go with a neutral gray, or maybe a complementary color? **Recommendation**: I'd suggest a neutral gray for secondary buttons—it's the most versatile and professional. It pairs well with any primary color and clearly signals 'less important action' to users. Most successful apps (like Stripe, Linear, Vercel) use gray for secondary."
- [ ] Ask about text color with readability guidance: "What color should text be on secondary buttons? **Recommendation**: Dark text on light gray buttons is standard—think of how Apple, Google, and Microsoft do it. It's instantly recognizable as a secondary action."
- [ ] Ask for dark mode with consistency guidance: "For dark mode, should the secondary be lighter or darker? **Recommendation**: Keep the same relationship—if it's light gray in light mode, use dark gray in dark mode. Maintain that visual hierarchy."

#### Muted Colors (Subtle Backgrounds)
- [ ] Ask about muted colors with UX principles: "For subtle backgrounds (like when you hover over items), what works? Usually something very light and neutral. Think of GitHub's light gray hover, or Notion's barely-there background change. **Recommendation**: I'd recommend something very subtle—about 2-3% darker or lighter than your background. It should be noticeable but not distracting. Too strong and it competes with your content; too subtle and users won't notice the feedback."
- [ ] Ask for dark mode with consistency: "For dark mode, the muted color should be... **Recommendation**: In dark mode, make it slightly lighter than your dark background. This creates the same subtle hover effect that users expect."

#### Accent Colors
- [ ] Ask about accent with design system guidance: "Any accent color for highlights? Like when something is emphasized or selected. Apple uses blue, some apps use your primary color, others use a complementary shade. **Recommendation**: I'd suggest using your primary color for accents—it creates consistency and reinforces your brand. If you want something different, a blue accent is universally recognized for 'active' or 'selected' states (think iOS, macOS, Windows)."
- [ ] Ask for dark mode: "For dark mode, should the accent adjust? **Recommendation**: Keep it consistent with light mode, but you might want to brighten it slightly so it stands out on dark backgrounds."

#### Error/Destructive Colors
- [ ] Ask about destructive with safety guidance: "What color should errors and destructive actions use? Usually red, but what shade? Stripe uses a softer red, Gmail uses a bold red, some apps use coral or orange-red. **Recommendation**: For destructive actions (like delete), I'd recommend a clear, recognizable red—not too orange, not too pink. Users need to instantly understand it's a warning. For errors and validation messages, a slightly softer red works well and feels less harsh. Think Stripe's error messages versus Gmail's delete button—both red, but different intensities for different purposes."
- [ ] Ask for dark mode: "For dark mode, should destructive colors be brighter? **Recommendation**: Yes, I'd suggest making destructive red slightly brighter in dark mode so it maintains the same visual weight and urgency."

#### Success & Warning Colors
- [ ] Ask about success color with positive feedback guidance: "For success messages and positive feedback, what color should we use? Usually green, but what shade works for your brand? Think about success checkmarks, 'saved successfully' messages, or positive notifications. Stripe uses a softer green, GitHub uses a clear emerald green, some apps go with a vibrant lime. **Recommendation**: I'd recommend a clear, recognizable green—not too yellow (can feel cautionary), not too blue (can feel like info). A classic green or emerald works well. Think of GitHub's success states or Stripe's success notifications—they're instantly recognizable as positive feedback."
- [ ] Ask about warning color with caution guidance: "For warnings and cautionary messages, what color feels right? Usually amber or yellow, but what shade? Think about 'are you sure?' prompts, pending states, or 'this might take a while' messages. Some apps use warm amber, others use a brighter yellow, some go with orange-amber. **Recommendation**: I'd suggest a warm amber rather than pure yellow—it feels more cautionary and less urgent than your destructive red. Amber is universally understood as 'proceed with caution' without being as alarming as red. Think of browser security warnings or payment confirmations—they use amber/yellow to get attention without panic."
- [ ] Ask for dark mode with visibility: "For dark mode, should success and warning colors adjust? **Recommendation**: Yes, I'd suggest making both slightly brighter in dark mode so they maintain good contrast and visibility. Success green and warning amber both need to be clearly visible on dark backgrounds."

#### Borders and Inputs
- [ ] Ask about borders with modern design trends: "For borders and input fields, how visible should they be? Subtle and minimal, or more defined? Apple products have very subtle borders, while Material Design is more defined. **Recommendation**: I'd recommend subtle borders—they're more modern and less visually cluttered. The border should be noticeable when you need it (like around inputs) but fade into the background otherwise. Most successful modern apps use very subtle borders."
- [ ] Ask about input backgrounds with UX guidance: "Should input fields have a background color, or be transparent? **Recommendation**: I'd suggest a very light background (slightly darker than your main background). It helps define the input area and makes it clear where users should click. Too strong and it feels heavy; transparent can be confusing."
- [ ] Ask about focus rings with accessibility: "When someone clicks into an input, should there be a visible outline? **Recommendation**: Absolutely! This is important for accessibility. A subtle colored outline (usually your primary color) helps users with keyboards and screen readers navigate. Most apps use a 2-3px outline in the primary color."
- [ ] Ask for dark mode: "For dark mode, should borders be lighter or darker? **Recommendation**: Lighter borders work better in dark mode—they need to be visible against dark backgrounds, so a subtle white or light gray at low opacity is standard."

#### Chart Colors
- [ ] Ask about chart colors with data visualization best practices: "For charts and graphs, you'll need 5 colors. Want me to create a harmonious palette, or do you have specific colors in mind? I could do: a blue set, a warm set (oranges/reds), a cool set (blues/greens), or a rainbow. Like how Google Analytics uses blues and greens, or how GitHub Insights uses multiple colors. **Recommendation**: I'd strongly recommend a harmonious palette that works together. For best results, I'd suggest either: A) A monochromatic set (different shades of your primary color), B) A complementary set (colors that work well together), or C) A data-viz optimized palette (like those used by Google Analytics or Tableau). Avoid rainbow colors—they can be confusing and some colors don't translate well to charts."
- [ ] Offer to generate palette: "Would you like me to create a professional palette that works with your primary color? I can make sure all colors are distinguishable and accessible."
- [ ] Ask for dark mode with visibility guidance: "For dark mode charts, should colors be adjusted? **Recommendation**: Yes, I'd suggest slightly different shades for dark mode. Colors that look great on white can be hard to see on dark backgrounds. I'll adjust them to maintain good contrast while keeping the same color identity."

#### Sidebar Colors
- [ ] Ask about sidebar with navigation best practices: "If your app has a sidebar, what should it look like? Should it match the background, be darker, lighter, or have its own color? Slack has a dark sidebar, Notion has a light one that matches, Discord uses a distinct dark gray. **Recommendation**: I'd recommend a subtle distinction from the main background—about 5-10% different. This creates clear navigation hierarchy. Most successful apps use either: A) A slightly darker sidebar (like Linear, Vercel) which feels modern, or B) A matching sidebar with subtle borders (like Notion). Avoid making it too different—it should feel part of the same interface."
- [ ] Ask about sidebar text with readability: "What color should sidebar text be? **Recommendation**: Keep it high contrast for readability. If the sidebar is light, use dark text. If it's dark, use light text. Make sure it's easily scannable."
- [ ] Ask about active states: "When a sidebar item is selected, how should it stand out? **Recommendation**: Use your primary color for the active state—it's instantly recognizable and reinforces your brand. Add a subtle background tint and maybe an accent border."
- [ ] Ask for dark mode: "For dark mode, should the sidebar relationship stay the same? **Recommendation**: Keep the same relationship. If it's darker than main background in light mode, make it lighter than main background in dark mode. Maintain that visual separation."

#### Border Radius (Roundness)
- [ ] Ask about radius with modern design guidance: "How rounded should your buttons and cards be? From sharp corners to very rounded. **Recommendation**: I'd recommend slightly rounded corners (like 8-12px equivalent)—it's the modern standard. Sharp corners feel dated (think Windows 95), and very rounded can feel playful (great for consumer apps, maybe too casual for professional tools). Slightly rounded hits the sweet spot: modern, professional, and friendly. Think Linear, Vercel, Stripe—they all use subtle rounding."
- [ ] Give visual examples with recommendations:
  - "Sharp/angular" (like old Windows) - "Not recommended—feels dated"
  - "Slightly rounded" (like modern apps—most common) - "**Recommended**—professional and modern"
  - "Very rounded" (like Instagram stories) - "Good for playful/consumer apps"
  - "Pill-shaped" (like iOS buttons) - "Great for specific buttons, maybe too much for everything"
- [ ] Show industry examples: "Apple tends to be more rounded, Google is medium, most modern SaaS apps use subtle rounding. I'd suggest matching the modern SaaS style unless you have a specific reason to go more playful."

#### Shadows & Depth (Optional)
- [ ] Ask about shadows with depth guidance: "How much depth should your cards and buttons have? Shadows create a sense of layering and make elements feel 'lifted' off the page. You can go with no shadows (flat design), subtle shadows (like Apple), medium shadows (like Material Design), or more pronounced shadows (like some modern SaaS apps). **Recommendation**: I'd recommend subtle to medium shadows—they add depth without being distracting. Subtle shadows feel modern and clean (think Apple's design language), while medium shadows help distinguish interactive elements (think Material Design cards). Most professional apps use subtle shadows—they're noticeable but don't compete with your content."
- [ ] Give options with examples:
  - "None/Flat" (like some minimal designs) - "Very clean, but can feel flat"
  - "Subtle" (like Apple, Linear) - "**Recommended**—modern and elegant"
  - "Medium" (like Material Design, Vercel) - "Good for clear hierarchy"
  - "Prominent" (like some dashboards) - "Good for emphasis, but can feel heavy"
- [ ] Ask if they want to customize: "Want to add some subtle depth to your interface, or keep it flat? Most modern apps use subtle shadows—they help cards and buttons feel interactive without being obvious."
- [ ] If user says skip/optional: Accept "skip", "default", "subtle", or let them choose and note it's optional

#### Font Families
- [ ] Ask about font family with typography guidance: "What font family should represent your brand? Fonts have personality—some feel modern and tech-forward, others feel warm and approachable. You can browse all available fonts at [Google Fonts](https://fonts.google.com) to see your options.

**My recommendations** for different vibes:

**Modern & Professional:**
- **Inter** - Clean, geometric, excellent readability (used by GitHub, Linear, Vercel) - **Highly recommended for SaaS/professional apps**
- **Plus Jakarta Sans** - Modern, friendly, great for dashboards (used by many modern startups)
- **Manrope** - Crisp, professional, slightly playful edge

**Warm & Approachable:**
- **Poppins** - Friendly, rounded, very readable (used by many consumer apps)
- **Nunito Sans** - Warm, human, approachable
- **Work Sans** - Professional yet friendly

**Bold & Distinctive:**
- **Space Grotesk** - Unique, modern, slightly tech-forward
- **DM Sans** - Clean with character, great for branding

**Classic & Timeless:**
- **Roboto** - Google's font, very reliable (used by Material Design)
- **Open Sans** - Extremely readable, neutral personality

Right now you're using Geist, which is a great modern choice. Would you like to keep Geist, or explore something different from Google Fonts? If you want to browse, visit [fonts.google.com](https://fonts.google.com) and let me know what catches your eye!"

- [ ] Accept font name if user provides it: Accept common Google Fonts names (case-insensitive), variations like "Inter", "Inter Variable", "Inter Sans", etc.
- [ ] If user chooses to browse: "Take your time browsing [Google Fonts](https://fonts.google.com)! When you find something you like, just tell me the name and I'll set it up. I can also help narrow it down if you tell me what vibe you're going for—modern, friendly, professional, etc."
- [ ] Ask about monospace font (optional): "For code or technical content, we also need a monospace font. Right now you have Geist Mono. Would you like to keep it, or change it? Some popular choices are: JetBrains Mono (tech-forward), Fira Code (great for coding), Source Code Pro (clean), or IBM Plex Mono (professional). **Recommendation**: If you're building a developer tool or have code snippets, I'd suggest JetBrains Mono or Fira Code—they're optimized for reading code. Otherwise, Geist Mono or Source Code Pro work great for general use."
- [ ] Confirm understanding: "So you want [font name] for your main font—that'll give your app a [describe personality] feel. Does that sound right?"

### 3. Collect and Validate Answers

**User-Friendly Input Handling:**
- [ ] Accept plain English descriptions ("bright blue", "soft gray", "warm orange")
- [ ] Accept comparisons ("like Instagram purple", "similar to Twitter blue")
- [ ] Accept relative changes ("darker", "brighter", "more muted")
- [ ] Accept hex codes IF user provides them (convert silently, don't ask for them)
- [ ] For radius: "sharp", "slightly rounded", "medium", "rounded", "very rounded", "pill-shaped"
- [ ] For shadows: Accept "none", "subtle", "medium", "prominent", "flat", "default", or "skip"
- [ ] For fonts: Accept Google Font names (case-insensitive), variations like "Inter", "Inter Variable", "Plus Jakarta Sans", etc. If font not found on Google Fonts, suggest similar alternatives
- [ ] Map user descriptions to OKLCH values behind the scenes
- [ ] Map shadow preferences to CSS shadow values (none = no shadows, subtle = small shadows, medium = medium shadows, prominent = larger shadows)
- [ ] Map font names to Next.js font imports (use Next.js Google Fonts helper when available)
- [ ] Confirm understanding before moving on: "So you want a bright, energetic blue—like Facebook blue but maybe a bit lighter?"
- [ ] If unclear, offer 2-3 specific options: "Would you prefer: A) A bright blue like Facebook, B) A deeper blue like LinkedIn, or C) Something in between?"

### 4. Update Design Tokens (Technical, Behind the Scenes)

- [ ] Create backup of `app/globals.css` before changes
- [ ] Create backup of `app/layout.tsx` before font changes
- [ ] Convert all user descriptions to OKLCH format internally
- [ ] Update `:root` section with light mode values
- [ ] Update `.dark` section with dark mode values
- [ ] Update `--radius` value (convert descriptions like "slightly rounded" to rem values)
- [ ] Add success and warning color tokens if user selected them:
  - [ ] Add `--success` and `--success-foreground` to `:root` and `.dark`
  - [ ] Add `--warning` and `--warning-foreground` to `:root` and `.dark`
  - [ ] Add success/warning color mappings to `@theme inline` section
- [ ] Add shadow tokens if user customized shadows (optional):
  - [ ] Define shadow scale in `@theme inline` or as CSS variables if needed
  - [ ] Note: Tailwind provides default shadows, only customize if user specifically requests it
- [ ] Preserve all CSS formatting and structure
- [ ] Maintain all existing CSS rules
- [ ] Update `app/layout.tsx` with selected font family:
  - [ ] Import selected font from `next/font/google` (or use appropriate Next.js font helper)
  - [ ] Handle font name variations (e.g., "Inter" → `Inter`, "Plus Jakarta Sans" → `Plus_Jakarta_Sans`)
  - [ ] Set font variable name (e.g., `--font-geist-sans` or `--font-{font-name}`)
  - [ ] Apply font variable to body className
  - [ ] Update monospace font if changed
  - [ ] Update font variables in `globals.css` `@theme inline` section if variable names change
  - [ ] Preserve existing font setup structure and formatting

### 5. Create Component Demo

After saving changes, create a demo page:

- [ ] Create `app/design-system-demo/page.tsx` (temporary demo page)
- [ ] Dynamically discover all components in `components/ui/` folder (check which components actually exist in the project)
- [ ] Show ALL available components using new design tokens, organized by category:

#### Navigation & Layout Components:
  - [ ] **Sidebar** - Show sidebar component with navigation items and active states
  - [ ] **Navigation Menu** - Display navigation menu with dropdowns (if available)
  - [ ] **Breadcrumb** - Show breadcrumb navigation (if available)
  - [ ] **Menubar** - Display menubar component (if available)
  - [ ] **Tabs** - Show tab navigation with multiple variants (if available)
  - [ ] **Separator** - Display separator/dividers

#### Form & Input Components:
  - [ ] **Button** - All variants (default, secondary, destructive, outline, ghost, link) and sizes
  - [ ] **Input** - Text input fields with various states (default, focus, error, disabled)
  - [ ] **Textarea** - Multi-line text input (if available)
  - [ ] **Label** - Form labels
  - [ ] **Checkbox** - Checkbox inputs with various states
  - [ ] **Radio Group** - Radio button groups (if available)
  - [ ] **Switch** - Toggle switches
  - [ ] **Slider** - Range sliders (if available)
  - [ ] **Select** - Dropdown select menus
  - [ ] **Input OTP** - OTP/verification code inputs (if available)
  - [ ] **Calendar** - Date picker calendar (if available)
  - [ ] **Form** - Complete form with validation states (if available)

#### Feedback & Display Components:
  - [ ] **Alert** - Alert messages (info, warning, error, success variants)
  - [ ] **Alert Dialog** - Confirmation dialogs (if available)
  - [ ] **Badge** - All badge variants (default, secondary, destructive, outline)
  - [ ] **Toast** - Toast notifications (if available)
  - [ ] **Skeleton** - Loading skeleton states
  - [ ] **Progress** - Progress bars (if available)
  - [ ] **Loader** - Loading indicators (if available)

#### Overlay & Dialog Components:
  - [ ] **Dialog** - Modal dialogs
  - [ ] **Sheet** - Side sheet/drawer panels
  - [ ] **Drawer** - Bottom drawer panels
  - [ ] **Popover** - Popover overlays
  - [ ] **Tooltip** - Tooltip hovers
  - [ ] **Hover Card** - Hover card component (if available)
  - [ ] **Context Menu** - Right-click context menus (if available)
  - [ ] **Command** - Command palette/combobox (if available)

#### Data Display Components:
  - [ ] **Card** - Card components with header, content, footer
  - [ ] **Table** - Data tables with various row states
  - [ ] **Avatar** - User avatars (single, group, with fallback)
  - [ ] **Accordion** - Collapsible accordion sections (if available)
  - [ ] **Collapsible** - Collapsible content areas
  - [ ] **Aspect Ratio** - Aspect ratio containers (if available)
  - [ ] **Carousel** - Image/content carousels (if available)
  - [ ] **Chart** - Chart visualizations (if available)
  - [ ] **Pagination** - Pagination controls (if available)

#### Interactive Components:
  - [ ] **Toggle** - Toggle buttons (if available)
  - [ ] **Toggle Group** - Toggle button groups (if available)
  - [ ] **Resizable** - Resizable panels (if available)
  - [ ] **Scroll Area** - Custom scroll areas (if available)

#### Project-Specific Components (include if available):
  - [ ] **Chat Container** - Chat interface components (if available)
  - [ ] **Message** - Message display components (if available)
  - [ ] **Prompt Input** - Prompt/input components (if available)
  - [ ] **Prompt Suggestion** - Suggestion components (if available)
  - [ ] **Code Block** - Code display components (if available)
  - [ ] **Markdown** - Markdown renderer (if available)
  - [ ] **Sonner** - Toast notifications via Sonner (if available)
  - [ ] **Toaster** - Toast container (if available)

#### Design System Showcase:
  - [ ] **Typography Samples** - All heading levels (h1-h6), body text, captions, labels
  - [ ] **Color Swatches** - Show all color tokens (primary, secondary, muted, accent, destructive, success, warning) with their foreground colors
  - [ ] **Border Radius Examples** - Visual examples of rounded corners on buttons, cards, inputs
  - [ ] **Shadow Examples** - Show shadow variations on cards and buttons (if customized)
  - [ ] **Chart Color Palette** - Display chart color swatches in a grid

- [ ] Include light/dark mode toggle at top of page
- [ ] Organize components in collapsible sections or tabs for easy navigation
- [ ] Use shadcn/ui components exclusively
- [ ] Apply design system tokens (no hardcoded colors)
- [ ] Make demo page visually organized with clear sections and labels
- [ ] Add friendly note at top explaining it's a temporary preview
- [ ] Include component names/labels for each demo section
- [ ] Show component states (hover, active, disabled, focus) where applicable

### 6. Wrap Up

- [ ] Confirm changes saved (don't mention technical file names)
- [ ] Show demo page URL in friendly way: "I've created a preview page so you can see everything together!"
- [ ] Explain demo is temporary: "This preview page is just for you to see how it looks—you can delete it whenever you want"
- [ ] Celebrate completion: "All done! Your design system is ready to use."
- [ ] Offer to adjust: "If anything doesn't look quite right, just let me know and I can tweak it!"

## See Also

- **[Design](../engineer/design.md)**: Advanced design command
- **[Extract Design Tokens](extract-design-tokens.md)**: Extract tokens from designs
- **[Check Design Consistency](check-design-consistency.md)**: Verify design system compliance
- **[Build](../build.md)**: Build features with design system
- **[Review Design Implementation](review-design-implementation.md)**: Review implementation against design