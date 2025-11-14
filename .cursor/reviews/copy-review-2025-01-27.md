# Copy Review - Vibecamp Website
**Date:** January 27, 2025  
**Reviewer:** AI Assistant  
**Scope:** UI copy, error messages, help text, and marketing copy across all languages

## Executive Summary

**Overall Assessment:** The copy is generally clear and effective, but there are several critical issues that need attention:
- **Critical:** Hardcoded English text in components breaks internationalization
- **High:** Inconsistent messaging across languages (hero titles differ significantly)
- **High:** Location and currency inconsistencies
- **Medium:** Repetitive value propositions reduce impact
- **Medium:** Error messages lack specificity and aren't internationalized

## Critical Issues

### 1. Hardcoded English Text in Components

**Location:** Multiple components  
**Issue:** Several components have hardcoded English text that won't be translated

**Affected Files:**
- `components/waitlist-modal.tsx` (line 134): "Email Address" label
- `components/course-preview-modal.tsx` (line 111): "Next Event" text
- `app/[lang]/error.tsx` (lines 24-26, 31, 34): All error messages
- `app/[lang]/not-found.tsx` (lines 12-14, 18): All 404 messages

**Impact:** Users in French/German locales will see mixed languages, breaking the user experience.

**Recommendation:** Move all user-facing text to dictionary files.

---

### 2. Inconsistent Hero Titles Across Languages

**Location:** `app/[lang]/dictionaries/*.json` → `hero.title`

**Current State:**
- **English:** "Learn to ship apps faster than anyone else" (specific, action-oriented)
- **French:** "Libérez votre potentiel" (Unlock your potential - generic, inspirational)
- **German:** "Entfalte dein Potenzial" (Unfold your potential - generic, inspirational)

**Issue:** The messages convey completely different value propositions. English is specific about speed, while FR/DE are generic empowerment messages.

**Recommendation:** Align all languages to the English version's specificity:
- **French:** "Apprenez à créer des applications plus rapidement que quiconque"
- **German:** "Lerne, Apps schneller als alle anderen zu erstellen"

---

### 3. Location Inconsistencies

**Location:** `joinCohort.importantInfo.inPersonOnly` and `inPersonDescription`

**Issue:** 
- French version (line 447): Says "San Francisco" but should be "Freiburg Im Breisgau"
- German version (line 447): Also says "San Francisco" instead of correct location

**Impact:** Users will be confused about where the workshop actually takes place.

**Recommendation:** Update all language versions to reflect the correct location: "Freiburg Im Breisgau, Germany"

---

### 4. Currency Format Inconsistencies

**Location:** Multiple places in dictionaries

**Current State:**
- "99euros" (no space, no symbol)
- "99 euros" (space, no symbol)
- "99 Euro" (capitalized, no symbol)
- "€99" or "249€" (with symbol)
- "$350 USD" (in French version)

**Issue:** Inconsistent formatting makes pricing look unprofessional.

**Recommendation:** Standardize to: "€99" or "99 €" (choose one format and use consistently)

---

## High Priority Issues

### 5. Repetitive Value Propositions

**Location:** Multiple sections across dictionaries

**Issue:** The phrase "Build full-stack applications with AI features using Next.js, Supabase, Vercel, and an AI SDK—the best tools available to build high-quality software" appears verbatim in:
- Hero description
- Job cards descriptions
- Single card description
- FAQ answers
- About page

**Impact:** Repetition reduces impact and makes copy feel templated rather than thoughtfully crafted.

**Recommendation:** 
- Keep the full version in 1-2 key places (hero, about page)
- Use shorter, varied versions elsewhere:
  - "Build with the best tools: Next.js, Supabase, Vercel, and AI SDK"
  - "Modern stack, AI-powered, production-ready"
  - "Industry-leading tools for rapid development"

---

### 6. Vague Call-to-Actions

**Location:** `hero.cta`

**Current:** "Explore Opportunities"

**Issue:** Too vague. Doesn't clearly indicate what action the user should take.

**Recommendation:** More specific CTAs:
- "Browse Courses"
- "View Courses"
- "See What's Available"
- Or remove if hero button is the primary CTA

---

### 7. Inconsistent Button Text

**Location:** Various buttons

**Issues:**
- "Join Now" vs "Join Waitlist" - different actions, similar wording
- "Secure Your Spot Now" - very long for a button
- "Rejoindre maintenant" vs "Rejoindre la liste d'attente" - same inconsistency in French

**Recommendation:** 
- Use distinct, action-specific labels:
  - Waitlist: "Join Waitlist" / "Rejoindre la liste"
  - Registration: "Register Now" / "S'inscrire maintenant"
  - Course preview: "View Details" / "Voir les détails"

---

## Medium Priority Issues

### 8. Error Messages Lack Specificity

**Location:** `app/[lang]/error.tsx`

**Current:**
- "Something went wrong!"
- "We encountered an unexpected error. Please try again."

**Issue:** Generic messages don't help users understand what happened or what to do.

**Recommendation:** Add to dictionaries with more helpful messaging:
```json
{
  "error": {
    "title": "Something went wrong",
    "description": "We're sorry, but something unexpected happened. Please try again, or return to the home page.",
    "tryAgain": "Try again",
    "goHome": "Go home"
  }
}
```

---

### 9. Tone Inconsistencies

**Issue:** Copy mixes very technical language with very accessible language:
- Technical: "full-stack applications", "AI SDK", "backend-as-a-service"
- Accessible: "No coding experience required", "Just bring your creativity"

**Impact:** Can confuse users about the target audience and skill level required.

**Recommendation:** 
- Decide on primary tone: Technical but accessible, or Accessible with technical details
- Use consistent terminology throughout
- Consider adding a glossary or tooltips for technical terms

---

### 10. Waitlist Modal Description

**Location:** `waitlistModal.description`

**Current (EN):** "Once you join the list we will get in contact to organise the course together."

**Issues:**
- Grammar: "we will get in contact" → "we will contact you"
- Unclear: "organise the course together" is vague

**Recommendation:** 
- "We'll contact you soon to help you choose the right course."
- "We'll reach out to discuss course options that fit your goals."

---

### 11. Course Price Formatting

**Location:** Course details

**Issue:** Prices like "99euros" should be formatted as currency.

**Recommendation:** Use proper currency formatting: "€99" or "99 €"

---

## Low Priority / Suggestions

### 12. Testimonial Authenticity

**Location:** `testimonialSection.testimonials`

**Note:** Testimonials are well-written and specific. Consider adding:
- Company names (if permission granted)
- More diverse backgrounds
- Specific metrics/results

---

### 13. FAQ Answer Length

**Location:** `faqSection.faqs`

**Note:** Some FAQ answers are quite long. Consider:
- Breaking into shorter paragraphs
- Using bullet points for key benefits
- Adding "Learn more" links to detailed pages

---

### 14. Course Descriptions

**Location:** Course details

**Note:** Course descriptions are clear and benefit-focused. Consider:
- Adding "What you'll need" sections
- Including prerequisites more clearly
- Adding "Who this is NOT for" to set expectations

---

## Recommendations Summary

### Immediate Actions (Critical)
1. ✅ Move all hardcoded text to dictionaries
2. ✅ Align hero titles across all languages
3. ✅ Fix location inconsistencies (San Francisco → Freiburg)
4. ✅ Standardize currency formatting

### Short-term (High Priority)
5. ✅ Reduce repetitive value propositions
6. ✅ Clarify CTAs
7. ✅ Standardize button text
8. ✅ Improve error messages

### Medium-term (Enhancement)
9. ✅ Establish consistent tone guidelines
10. ✅ Improve waitlist modal copy
11. ✅ Add glossary/tooltips for technical terms

---

## Positive Highlights

✅ **Clear value propositions** - Users understand what they'll get  
✅ **Strong testimonials** - Specific and credible  
✅ **Good FAQ coverage** - Addresses common concerns  
✅ **Accessible language** - Most copy is easy to understand  
✅ **Action-oriented** - CTAs are generally clear about next steps  

---

## Next Steps

1. **Create internationalized error/404 pages** - Move hardcoded text to dictionaries
2. **Standardize hero messaging** - Align all language versions
3. **Fix location/currency inconsistencies** - Update all affected entries
4. **Create copy style guide** - Document tone, terminology, and formatting standards
5. **A/B test CTAs** - Test different button text for conversion

---

## Files Requiring Updates

### Critical Updates Needed:
- `app/[lang]/dictionaries/en.json`
- `app/[lang]/dictionaries/fr.json`
- `app/[lang]/dictionaries/de.json`
- `components/waitlist-modal.tsx`
- `components/course-preview-modal.tsx`
- `app/[lang]/error.tsx`
- `app/[lang]/not-found.tsx`

### Recommended New Files:
- `.cursor/rules/copy-style-guide.mdc` - Document copy standards
- `app/[lang]/dictionaries/error-messages.json` - Centralized error copy


