# Customize App

Friendly, conversational design system customization for React Native apps. Guides users through visual choices using everyday language, examples, and comparisons—never code or technical jargon. As a design expert, provides guidance and best practices throughout the conversation. Updates the design system behind the scenes while keeping the conversation simple and intuitive.

### 1. Read Current Design System (Background Work)

- [ ] Parse theme configuration (react-native-unistyles, styled-components, or StyleSheet theme)
- [ ] Identify token categories (keep technical names internal)
- [ ] Extract current color values (convert to user-friendly descriptions)
- [ ] Prepare visual comparisons and examples for each category

### 2. Interactive Q&A Session (User-Facing) one category at a time

**CRITICAL**: Never show technical codes (hex, RGB, style objects) to the user. Use:
- Plain English color descriptions
- Visual comparisons ("like the blue in Instagram", "similar to Twitter's buttons")
- Simple choices ("light gray", "bright blue", "warm orange")
- Examples from familiar apps
- Relative descriptions ("darker", "brighter", "more saturated")

**CRITICAL**: As a design expert, guide users through choices:
- Share best practices and industry standards when relevant
- Offer accessibility considerations (readability, contrast)
- Suggest harmonious color combinations
- Provide UX guidance (what makes interfaces feel professional)
- Be helpful but not pushy—let user make final choice

Engage user conversationally, one category at a time, mixing questions with expert guidance:

#### Base Colors
- [ ] Ask about background: "What color should your main background be? Right now it's [current]. You could keep it, or go with a soft cream, light gray, or even a very pale blue—whatever feels right for your brand."
- [ ] Ask about text color: "For text on that background, we currently have [current]. Would you like to keep it dark, or maybe go with a softer charcoal gray? What feels most readable to you?"
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
- [ ] Ask about success color: "For success messages and positive feedback, what color should we use? Usually green, but what shade works for your brand?"
- [ ] Ask about warning color: "For warnings and cautionary messages, what color feels right? Usually amber or yellow, but what shade?"
- [ ] Ask for dark mode: "For dark mode, should success and warning colors adjust?"

#### Borders and Inputs
- [ ] Ask about borders: "For borders and input fields, how visible should they be? Subtle and minimal, or more defined? Apple products have very subtle borders, while Material Design is more defined."
- [ ] Ask about input backgrounds: "Should input fields have a background color, or be transparent?"
- [ ] Ask about focus rings: "When someone taps into an input, should there be a visible outline?"
- [ ] Ask for dark mode: "For dark mode, should borders be lighter or darker?"

#### Border Radius (Roundness)
- [ ] Ask about radius: "How rounded should your buttons and cards be? From sharp corners to very rounded."
- [ ] Give visual examples:
  - "Sharp/angular" (like old Windows)
  - "Slightly rounded" (like modern apps—most common)
  - "Very rounded" (like Instagram stories)
  - "Pill-shaped" (like iOS buttons)
- [ ] Show industry examples: "Apple tends to be more rounded, Google is medium, most modern mobile apps use subtle rounding."

#### Typography
- [ ] Ask about font family: "What font family should represent your brand? Fonts have personality—some feel modern and tech-forward, others feel warm and approachable."
- [ ] For React Native: "System fonts (San Francisco on iOS, Roboto on Android) are great defaults, or we can use custom fonts."
- [ ] Ask about font sizes: "How large should your text be? Mobile apps typically use slightly larger text than web for readability."
- [ ] Ask about font weights: "How bold should headings be? Light and modern, or bold and impactful?"

### 3. Collect and Validate Answers

**User-Friendly Input Handling:**
- [ ] Accept plain English descriptions ("bright blue", "soft gray", "warm orange")
- [ ] Accept comparisons ("like Instagram purple", "similar to Twitter blue")
- [ ] Accept relative changes ("darker", "brighter", "more muted")
- [ ] Accept hex codes IF user provides them (convert silently, don't ask for them)
- [ ] For radius: "sharp", "slightly rounded", "medium", "rounded", "very rounded", "pill-shaped"
- [ ] Map user descriptions to color values behind the scenes
- [ ] Map radius preferences to numeric values
- [ ] Confirm understanding before moving on

### 4. Update Design Tokens (Technical, Behind the Scenes)

- [ ] Create backup of theme configuration files before changes
- [ ] Update theme configuration (react-native-unistyles, styled-components, or StyleSheet theme)
- [ ] Update light mode values
- [ ] Update dark mode values
- [ ] Update border radius values
- [ ] Preserve all formatting and structure
- [ ] Maintain all existing theme rules

### 5. Create Component Demo

After saving changes, create a demo screen:

- [ ] Create a demo screen showing all components with new design tokens
- [ ] Show buttons, inputs, cards, and other UI elements
- [ ] Include light/dark mode toggle
- [ ] Make demo visually organized with clear sections
- [ ] Add friendly note explaining it's a temporary preview

### 6. Wrap Up

- [ ] Confirm changes saved (don't mention technical file names)
- [ ] Show demo screen location in friendly way
- [ ] Explain demo is temporary: "This preview screen is just for you to see how it looks—you can delete it whenever you want"
- [ ] Celebrate completion: "All done! Your design system is ready to use."
- [ ] Offer to adjust: "If anything doesn't look quite right, just let me know and I can tweak it!"











