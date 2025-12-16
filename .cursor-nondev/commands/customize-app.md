# Customize App

Friendly, conversational design system customization for non-technical users. Guides them through visual choices using everyday language, examples, and comparisons—never code or technical jargon. As a design expert, provides guidance and best practices throughout the conversation. Updates the design system behind the scenes while keeping the conversation simple and intuitive.

### 1. Read Current Design System (Background Work)

- [ ] Parse `app/globals.css` to extract all design tokens (don't mention this to user)
- [ ] Identify token categories (keep technical names internal)
- [ ] Extract current color values (convert to user-friendly descriptions)
- [ ] Prepare visual comparisons and examples for each category

### 2. Interactive Q&A Session (User-Facing) one category at a time

**CRITICAL**: Never show technical codes (OKLCH, hex, CSS) to the user. Use:
- Plain English color descriptions
- Visual comparisons ("like the blue in Facebook", "similar to Twitter's buttons")
- Simple choices ("light gray", "bright blue", "warm orange")
- Examples from familiar apps and websites
- Relative descriptions ("darker", "brighter", "more saturated")

**CRITICAL**: As a design expert, guide users through choices:
- Share best practices and industry standards when relevant
- Offer accessibility considerations (readability, contrast)
- Suggest harmonious color combinations
- Provide UX guidance (what makes interfaces feel professional)
- Be helpful but not pushy—let user make final choice

Engage user conversationally, one category at a time, mixing questions with expert guidance:

#### Base Colors
- [ ] Ask about background: "What color should your main background be? Right now it's pure white. You could keep it white, or go with a soft cream, light gray, or even a very pale blue—whatever feels right for your brand."
- [ ] Ask about text color: "For text on that background, we currently have almost-black. Would you like to keep it dark, or maybe go with a softer charcoal gray? What feels most readable to you?"
- [ ] Ask about cards: "Cards (like these boxes with content) can match the background or be slightly different. What do you prefer?"
- [ ] Ask about dark mode: "When it's dark, do you want a true black, dark gray, or maybe a deep navy blue?"

#### Primary Colors (Main Brand Color)
- [ ] Ask about brand color with examples: "What's the main color that represents your brand? This is the color for your most important buttons and links. Like how Instagram uses purple, Spotify uses green, or LinkedIn uses blue. What color feels like 'you'?"
- [ ] Provide saturation guidance: "How bright or subtle should it be? Bold and energetic, or calm and professional?"
- [ ] Ask about text on primary: "When text sits on top of that color, should it be white, black, or something in between?"
- [ ] Ask for dark mode: "For dark mode, should we use the same primary color or adjust it?"

#### Secondary Colors
- [ ] Ask about secondary: "For your secondary buttons and accents, what color works? This should complement your primary color. Some apps use a softer version of the primary, others go with a neutral gray, or maybe a complementary color?"
- [ ] Ask about text color: "What color should text be on secondary buttons?"
- [ ] Ask for dark mode: "For dark mode, should the secondary be lighter or darker?"

#### Muted Colors (Subtle Backgrounds)
- [ ] Ask about muted colors: "For subtle backgrounds (like when you hover over items), what works? Usually something very light and neutral. Think of GitHub's light gray hover, or Notion's barely-there background change."
- [ ] Ask for dark mode: "For dark mode, the muted color should be..."

#### Accent Colors
- [ ] Ask about accent: "Any accent color for highlights? Like when something is emphasized or selected. Apple uses blue, some apps use your primary color, others use a complementary shade."
- [ ] Ask for dark mode: "For dark mode, should the accent adjust?"

#### Error/Destructive Colors
- [ ] Ask about destructive: "What color should errors and destructive actions use? Usually red, but what shade? Stripe uses a softer red, Gmail uses a bold red, some apps use coral or orange-red."
- [ ] Ask for dark mode: "For dark mode, should destructive colors be brighter?"

#### Success & Warning Colors
- [ ] Ask about success color: "For success messages and positive feedback, what color should we use? Usually green, but what shade works for your brand? Think about success checkmarks, 'saved successfully' messages, or positive notifications. Stripe uses a softer green, GitHub uses a clear emerald green, some apps go with a vibrant lime."
- [ ] Ask about warning color: "For warnings and cautionary messages, what color feels right? Usually amber or yellow, but what shade? Think about 'are you sure?' prompts, pending states, or 'this might take a while' messages. Some apps use warm amber, others use a brighter yellow, some go with orange-amber."
- [ ] Ask for dark mode: "For dark mode, should success and warning colors adjust?"

#### Borders and Inputs
- [ ] Ask about borders: "For borders and input fields, how visible should they be? Subtle and minimal, or more defined? Apple products have very subtle borders, while Material Design is more defined."
- [ ] Ask about input backgrounds: "Should input fields have a background color, or be transparent?"
- [ ] Ask about focus rings: "When someone clicks into an input, should there be a visible outline?"
- [ ] Ask for dark mode: "For dark mode, should borders be lighter or darker?"

#### Chart Colors
- [ ] Ask about chart colors: "For charts and graphs, you'll need 5 colors. Want me to create a harmonious palette, or do you have specific colors in mind? I could do: a blue set, a warm set (oranges/reds), a cool set (blues/greens), or a rainbow. Like how Google Analytics uses blues and greens, or how GitHub Insights uses multiple colors."
- [ ] Offer to generate palette: "Would you like me to create a professional palette that works with your primary color? I can make sure all colors are distinguishable and accessible."
- [ ] Ask for dark mode: "For dark mode charts, should colors be adjusted?"

#### Sidebar Colors
- [ ] Ask about sidebar: "If your app has a sidebar, what should it look like? Should it match the background, be darker, lighter, or have its own color? Slack has a dark sidebar, Notion has a light one that matches, Discord uses a distinct dark gray."
- [ ] Ask about sidebar text: "What color should sidebar text be?"
- [ ] Ask about active states: "When a sidebar item is selected, how should it stand out?"
- [ ] Ask for dark mode: "For dark mode, should the sidebar relationship stay the same?"

#### Border Radius (Roundness)
- [ ] Ask about radius: "How rounded should your buttons and cards be? From sharp corners to very rounded."
- [ ] Give visual examples:
  - "Sharp/angular" (like old Windows)
  - "Slightly rounded" (like modern apps—most common)
  - "Very rounded" (like Instagram stories)
  - "Pill-shaped" (like iOS buttons)
- [ ] Show industry examples: "Apple tends to be more rounded, Google is medium, most modern SaaS apps use subtle rounding."

#### Shadows & Depth (Optional)
- [ ] Ask about shadows: "How much depth should your cards and buttons have? Shadows create a sense of layering and make elements feel 'lifted' off the page. You can go with no shadows (flat design), subtle shadows (like Apple), medium shadows (like Material Design), or more pronounced shadows (like some modern SaaS apps)."
- [ ] Give options with examples:
  - "None/Flat" (like some minimal designs)
  - "Subtle" (like Apple, Linear)
  - "Medium" (like Material Design, Vercel)
  - "Prominent" (like some dashboards)
- [ ] Ask if they want to customize: "Want to add some subtle depth to your interface, or keep it flat? Most modern apps use subtle shadows—they help cards and buttons feel interactive without being obvious."
- [ ] If user says skip/optional: Accept "skip", "default", "subtle", or let them choose and note it's optional

#### Font Families
- [ ] Ask about font family: "What font family should represent your brand? Fonts have personality—some feel modern and tech-forward, others feel warm and approachable. You can browse all available fonts at [Google Fonts](https://fonts.google.com) to see your options.

Right now you're using Geist, which is a great modern choice. Would you like to keep Geist, or explore something different from Google Fonts? If you want to browse, visit [fonts.google.com](https://fonts.google.com) and let me know what catches your eye!"

- [ ] Accept font name if user provides it: Accept common Google Fonts names (case-insensitive), variations like "Inter", "Inter Variable", "Inter Sans", etc.
- [ ] If user chooses to browse: "Take your time browsing [Google Fonts](https://fonts.google.com)! When you find something you like, just tell me the name and I'll set it up. I can also help narrow it down if you tell me what vibe you're going for—modern, friendly, professional, etc."
- [ ] Ask about monospace font (optional): "For code or technical content, we also need a monospace font. Right now you have Geist Mono. Would you like to keep it, or change it? Some popular choices are: JetBrains Mono (tech-forward), Fira Code (great for coding), Source Code Pro (clean), or IBM Plex Mono (professional)."
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

### 5. Collect Design Inspirations

After updating all global CSS elements, ask about design inspirations:

- [ ] Ask conversationally: "Great! Your design system is looking good. Now, which products or websites inspire you? These will be added to your design references so you can study their patterns when building new features. You can name 1-3 products—like Airbnb, OpenAI, Linear, Stripe, or any others that resonate with your vision."
- [ ] Accept user input: Allow user to provide 1-3 product/website names
- [ ] If user provides inspirations:
  - [ ] Ask for brief descriptions (optional): "What do you like about [product name]? Is it their clean interface, smooth interactions, or something else? This helps understand what patterns to reference."
  - [ ] Accept brief descriptions or skip if user doesn't want to elaborate
- [ ] If user doesn't provide inspirations or wants defaults:
  - [ ] Use default inspirations: Airbnb, OpenAI, Dia Browser
  - [ ] Explain defaults: "No problem! I'll set up some great defaults: Airbnb (excellent search and filtering), OpenAI (clean AI interfaces), and Dia Browser (modern browser patterns). You can always update these later."
- [ ] Update `.cursor/rules/ui-ui-designer.mdc`:
  - [ ] Read current Design Inspirations section
  - [ ] Replace or update the "Default references" list with user-provided inspirations (or keep defaults if none provided)
  - [ ] For each inspiration, add a brief description of what makes it valuable:
    - If user provided descriptions, use those
    - If defaults, use existing descriptions (Airbnb, OpenAI, Dia Browser)
    - If new products without descriptions, create brief descriptions based on common patterns (e.g., "Clean interface design, thoughtful interactions, modern UI patterns")
  - [ ] Preserve the "How to use" subsection structure
  - [ ] Maintain markdown formatting and structure
- [ ] Confirm update: "Perfect! I've added [list inspirations] to your design references. You can find them in your design guidelines, and they'll help guide your design decisions going forward."

### 6. Create Component Demo

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

### 7. Wrap Up

- [ ] Confirm changes saved (don't mention technical file names)
- [ ] Show demo page URL in friendly way: "I've created a preview page so you can see everything together!"
- [ ] Explain demo is temporary: "This preview page is just for you to see how it looks—you can delete it whenever you want"
- [ ] Celebrate completion: "All done! Your design system is ready to use."
- [ ] Offer to adjust: "If anything doesn't look quite right, just let me know and I can tweak it!"
