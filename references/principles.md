# The 15 Principles of Simple Web Design

Detailed breakdown of each principle, based on Anthony Hobday's "Simple Web Design".
Use this reference when giving thorough critiques or designing from scratch.

---

## 1. Content First

**The design should serve the content — not the other way around.**

Content is whatever the user came to see: an article, a product, a tool, data, a video. Everything
else is infrastructure. The measure of success is the **content-element ratio** — the proportion
of meaningful content relative to all elements on the page. High ratio = respect for the user.

**Common violations:**
- Hero sections with full-screen decorative photography that pushes content below the fold
- Splash animations or loading screens before static content
- Sidebar widgets (social feeds, tag clouds) that compete with the main article
- Stock photos of smiling people that communicate nothing

**Design guidance:**
- Reduce or eliminate decorative imagery; let product screenshots, user-generated content,
  or data visualizations serve double duty as both content and visual interest
- Ask: "If I removed this element, would the user miss it?" If no → remove it
- Instagram stripped color from its UI so photos pop. Apple Music made "the music the hero."
  These are content-first decisions at scale.

**Code signals:**
```css
/* Bad: decorative overlay that fights content */
.hero { background: url(stock-photo.jpg); filter: brightness(0.5); }
.hero h1 { color: white; text-shadow: ... }

/* Better: the headline IS the hero */
.hero { background: white; padding: 4rem 2rem; }
.hero h1 { font-size: 3rem; color: #111; }
```

---

## 2. Wordy

**Words are a design material — often the most powerful one.**

Don't cut words to appear "minimal." Cut words that don't add meaning. Clear labels eliminate
confusion that no amount of visual design can fix. Basecamp's principle: prefer good copywriting
and take time to explain things with words, instead of minimalist UIs with unlabeled buttons.

**Common violations:**
- Icon-only navigation without labels
- Buttons labeled "Go →" or "Submit" instead of "Start your free trial" or "Send message"
- Tooltips that explain what a button does (the tooltip text *should be the button label*)
- Marketing copy that sounds impressive but explains nothing ("Supercharge your workflow")

**Design guidance:**
- Label every interactive element with a verb phrase: "Download report", "Add team member"
- Replace ambiguous icons (hamburger, kebab menu) with explicit labels for primary actions
- Use headings and body text to explain the product — don't rely on images alone
- Write microcopy for error states, empty states, and confirmation messages

---

## 3. Minimal

**Include only what's necessary. Every added element increases cognitive load.**

Minimalism is not visual sparseness — it's functional restraint. Every element competes for
attention. The question isn't "should I add this?" but "does this earn its place?"

**Common violations:**
- Navigation with 8+ links when 4 would do
- Feature grids listing 20 features when the top 5 would convert better
- Cookie banners, newsletter pop-ups, live chat bubbles, and social proof banners — all
  fighting for attention simultaneously
- "Related articles" sections that appear before the user finishes the primary article

**Design guidance:**
- Audit every nav link: remove those that aren't used or could live elsewhere
- Apply progressive disclosure: surface the minimum needed to decide, then reveal depth on demand
- The rule of one: one hero message, one primary CTA, one key benefit per section

---

## 4. Typographic

**Typography is the primary design tool of the web.**

A well-typeset page with no images can be more beautiful — and more usable — than a visually
complex one. Strong hierarchy guides the eye without decoration.

**Rules:**
- Body text: **≥ 16px**, line-height **1.5–1.7**, max line length **60–80 characters**
- Maximum **2 typefaces**; usually 1 is enough
- Maximum **3 weights** (e.g., Regular 400, Medium 500, Bold 700)
- Hierarchy via **size and weight** — not just color
- Avoid ultra-light weights (300) for body copy — they hurt legibility at small sizes
- System fonts are a legitimate, high-performance choice

**Common violations:**
- Body text at 14px or smaller
- Using color as the primary differentiator between H1 and H2 (no size difference)
- 4+ different typefaces
- Full-width text lines on desktop (→ 100+ characters per line)

**Code signals:**
```css
/* Good typographic foundation */
body {
  font-family: system-ui, -apple-system, sans-serif;
  font-size: 1.125rem; /* 18px */
  line-height: 1.6;
  max-width: 68ch; /* ~65 characters */
  color: #1a1a1a;
}

h1 { font-size: 2.5rem; font-weight: 700; line-height: 1.2; }
h2 { font-size: 1.75rem; font-weight: 600; }
```

---

## 5. Modest

**Let the content speak. The design should not show off.**

Modesty means choosing the understated option when two choices are equally functional.
Parallax, 3D transforms, complex entrance animations — these are "look at me" choices.
They prioritize designer expression over user experience.

**Common violations:**
- Scroll-triggered animations on every section
- Glassmorphism cards, neumorphic buttons, gradient mesh backgrounds
- Horizontal scroll sections on desktop
- Cursor follower effects
- "We're different" design language that makes standard tasks harder

**Design guidance:**
- Motion should communicate state (loading, transition, feedback) — not decorate
- Remove animations that don't help users understand what happened or what's next
- Choose the plain background color over the complex gradient

---

## 6. Timeless

**Design for longevity, not the current trend.**

Trend-based design ages quickly and creates redesign debt. Timeless design uses proven patterns
that survive because they work — not because they're fashionable.

The Drudge Report has served millions of readers for decades on the same design. The lesson:
functional clarity outlasts aesthetic fashion.

**Trends to avoid committing to:**
- Bento grid layouts as the primary structure
- Glassmorphism / frosted glass cards
- Loud gradient text headers
- Dark mode-only designs
- Bubbly "friendly SaaS" illustration styles

**Timeless patterns to rely on:**
- Clear navigation (sticky header, visible links)
- One-column readable article layout
- Card grids with consistent spacing
- Color schemes: black + white + one accent
- Left-aligned text and labels

---

## 7. Materially Honest

**Don't fake affordances you don't have. Don't hide affordances you do.**

Skeuomorphic textures and 3D effects imply physical properties the interface doesn't have.
Flat design stripped these out — but sometimes went too far, making clickable things invisible.
The goal: elements should *accurately communicate* their interactive nature.

**Common violations:**
- Buttons that look like plain text (no border, background, or underline)
- Non-interactive sections styled to look like UI cards (confusion about clickability)
- Links that look like regular text (no color differentiation or underline)
- Decorative elements that look like they should be interactive

**Design guidance:**
- Interactive: consistent visual treatment (color, border, or underline for links; background + border-radius for buttons)
- Non-interactive: visually inert (no hover cursor, no border that implies a card)
- Hover states and focus rings are features — not optional polish

---

## 8. Easy to Implement

**If a design is too complex to build, it won't be built well.**

Design complexity compounds into code complexity: edge cases, state management, browser bugs,
performance regressions. The simplest design that achieves the goal is always the best design.

**Common violations:**
- Full-screen canvas animations for backgrounds
- Complex masonry or irregular grid layouts
- Designs that require JavaScript for basic layout
- Multi-step transitions requiring precise timing coordination

**Design guidance:**
- Prefer CSS Grid/Flexbox over absolute positioning
- Design in standard breakpoints (mobile 375px, tablet 768px, desktop 1280px)
- Components should be stateless where possible
- Build for the developer who maintains this 2 years from now

---

## 9. Commercially Valuable

**Simplicity converts. Clutter distracts from the action you want users to take.**

Visual polish cannot compensate for a weak or unclear value proposition. The "story" — what you
do, who it's for, why it matters — must come through in plain language before design enhances it.

**Common violations:**
- Multiple competing CTAs above the fold ("Start free trial" / "Watch demo" / "Talk to sales" / "Read docs")
- Hero headline that's clever but doesn't explain the product
- Social proof sections with unnamed/unattributed quotes
- Pricing pages that bury the price in a footnote

**Design guidance:**
- Primary CTA visible above the fold, visually dominant
- Hero headline: 8–12 words, plain language, states who this is for and what they get
- One primary CTA per page section; secondary actions visually subordinate
- Testimonials: full name, company, role, photo — specific outcomes preferred

---

## 10. Performant

**A fast page is a better page. Performance is UX.**

Every additional font file, script, image, and third-party embed has a cost: load time, battery,
data. Slow pages increase bounce rate, reduce trust, and hurt SEO.

**Benchmarks:**
- Time to Interactive: < 2s on broadband, < 5s on 4G
- Largest Contentful Paint (LCP): < 2.5s
- Cumulative Layout Shift (CLS): < 0.1
- Total page weight: < 1MB for landing pages

**Common violations:**
- Loading Google Fonts + 3 custom fonts + a display typeface = 4 font families
- Uncompressed hero images (1MB+ JPEGs)
- A dozen third-party analytics/tracking scripts
- Heavy JS framework rendering mostly static content

**Design guidance:**
- System fonts are zero-cost; use them for body text
- Limit web fonts to 1 family, 2 weights, with `font-display: swap`
- Lazy-load all images below the fold; use WebP/AVIF
- Audit third-party scripts — each one adds latency

---

## 11. Accessible

**A design that excludes users has failed.**

Accessibility is also good SEO, good legal practice, and good design — because constraints that
help users with disabilities almost always help all users.

**Non-negotiables:**
- Text contrast ≥ 4.5:1 for body (WCAG AA); ≥ 3:1 for large text
- All interactive elements keyboard-navigable with visible focus states
- All images have descriptive `alt` text (decorative images: `alt=""`)
- Color is never the sole way to communicate meaning
- Tap targets ≥ 44×44px on mobile
- Forms: labels associated with inputs (`<label for="...">` or `aria-label`)

**Common violations:**
- `outline: none` on focused elements (killing keyboard navigation)
- Gray text on white background below 4.5:1 contrast
- Icon buttons without `aria-label`
- Placeholder text used as the only field label

---

## 12. Focused

**Each page should have one primary purpose.**

A page that tries to do everything does nothing well. Focus reduces decision fatigue, improves
conversion, and makes analytics meaningful (you can tell if the page is working).

**Common violations:**
- Landing page that's also a blog index that also has a product tour video
- Dashboard with 15 different "start here" entry points
- Product pages that promote the newsletter, the podcast, and a related product simultaneously

**Design guidance:**
- Define one primary action per page before designing anything
- Secondary actions should be smaller, lower on the page, or on separate pages
- Use progressive disclosure: summary → detail, not everything at once

---

## 13. Clear

**If users have to think about how to use the interface, it's not clear enough.**

Clarity reduces cognitive effort. Users should never wonder: "Where am I?", "What does this do?",
"What should I do next?", or "Did that work?"

**Common violations:**
- Navigation with jargon labels that don't match user mental models
- Error messages that say "Something went wrong" with no guidance
- Ambiguous button placement (is this save or cancel?)
- No loading/success/error feedback on form submissions

**Design guidance:**
- Use visual hierarchy to direct attention to the most important element first
- Show location: active nav states, breadcrumbs, step indicators
- Error messages: [what went wrong] + [what to do]. Example: "Email already in use — try signing in"
- Use the words your users use (check support tickets and reviews for vocabulary)

---

## 14. Distraction Free

**Remove everything that competes with the user's goal.**

Distractions are not just annoyances — they are conversion killers and trust destroyers.
Each distraction requires the user to spend cognitive resources deciding to ignore it.

**Common violations:**
- Autoplay video (with or without sound)
- Newsletter pop-up on page load (or within 5 seconds)
- Cookie consent banner that covers 40% of the viewport
- Sticky "chat with us" bubbles
- Social share widgets mid-article
- "You might also like" carousels before the current content is finished

**Design guidance:**
- Delay optional pop-ups until the user signals engagement (scroll past 80%, time > 60s)
- Provide a close button that's easy to hit (not 8px × 8px)
- Live chat widgets: hide on mobile, offer a delay before showing on desktop
- Social proof banners: bottom-of-page or only on specific conversion pages

---

## 15. Productive

**The interface should help users accomplish their goals in as few steps as possible.**

Every extra click, form field, page load, or modal is friction. Friction reduces completion rates.

**Common violations:**
- Account creation required before any product value is shown
- 7-field contact forms when name + email would do
- Search that returns results on a new page with no filtering
- Settings buried 3 levels deep in navigation

**Design guidance:**
- Streamline forms: only collect required information; batch optional fields to a later step
- Smart defaults: pre-select the most common option; remember previous choices
- Persistent, accessible navigation for frequently visited areas
- For complex flows: show progress, allow going back, save state between steps
- Consider "try before you sign up" flows — let users experience value first

---

*Source: Anthony Hobday, "Simple Web Design" — https://anthonyhobday.com/books/simpledesign/*
