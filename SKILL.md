---
name: simple-web-design
description: >
  Apply the principles of simple web design to critique, improve, or create website UI and UX.
  Use this skill whenever the user asks for feedback on a website, landing page, app interface,
  or any digital product design — even if they just say "does this look good?", "review my site",
  "how can I improve my UX", "is my layout clean?", "what's wrong with my homepage", or
  "help me design a web page". Also trigger when the user shares a URL or screenshot and wants
  design advice, or when writing copy/content for web interfaces. This skill draws from
  Anthony Hobday's "Simple Web Design" framework — 15 principles that prioritize content,
  clarity, and long-term usability over visual complexity and trend-chasing.
---

# Simple Web Design Skill

This skill applies Anthony Hobday's 15 principles of simple web design to help users
review, critique, or build websites and digital interfaces with better UI and UX.

---

## Core Philosophy

> "Good content has more impact on your success than the rest of the design."

Simple design is not "boring" design. It is *disciplined* design — where every element
earns its place by serving the user. The enemy of simple design is clutter, ego, and trend.

---

## The 15 Principles

Apply all relevant principles when reviewing or creating. Each principle includes a diagnostic
question — use these to structure feedback.

---

### 1. CONTENT FIRST
**The design should serve the content — not the other way around.**

- Ask: *Does anything on the page compete with the content for attention?*
- The content is whatever the user came to see: text, product, data, video.
- Remove or reduce any element (decorative images, gradients, animations) that doesn't make the content clearer.
- Maintain a high **content-element ratio**: the proportion of meaningful content vs. decorative/structural UI.
- Examples of content-first wins: Instagram stripping color from UI so photos pop; Apple Music making "the music the hero".

**Design guidance:**
- Reduce decorative imagery — let photos and product shots serve content purposes.
- Strip background patterns, hero illustrations, or stock photos that don't communicate.
- Prioritize text legibility and information hierarchy above aesthetic effects.

---

### 2. WORDY
**Words are a design material — often the most powerful one.**

- Ask: *Are there unlabeled icons, ambiguous buttons, or interactions that rely on the user guessing?*
- Prefer clear labels over minimalist iconography alone.
- Don't cut words to appear "clean" — cut words that don't add meaning.
- Good copywriting reduces UI complexity: a well-named button eliminates the need for a tooltip.

**Design guidance:**
- Label buttons clearly ("Start your free trial" > "Go" or an arrow icon).
- Use headings, subheadings, and body text to explain the product — don't rely on images to do all the communicating.
- If a UI element needs a tooltip to be understood, consider making the label the default.

---

### 3. MINIMAL
**Include only what's necessary. Every added element increases cognitive load.**

- Ask: *What happens if I remove this element? Would the user notice or benefit?*
- Minimalism is not visual sparseness — it's functional restraint.
- The test: could this page accomplish its goal with fewer elements?

**Design guidance:**
- Audit navigation: does every link in the nav need to be there?
- Remove social proof widgets, cookie banners, pop-ups, and chat bubbles that aren't mission-critical.
- Resist adding features or sections because they "might be useful."

---

### 4. TYPOGRAPHIC
**Typography is the primary design tool of the web.**

- Ask: *Does the type communicate a clear hierarchy? Is it comfortable to read?*
- A well-typeset page with no images can be more beautiful than a visually complex one.
- Strong typographic hierarchy (H1, H2, body, caption) guides the eye without decoration.

**Design guidance:**
- Use a maximum of 2 typefaces (often 1 is enough).
- Ensure body text is 16–18px minimum, with a line-height of 1.5–1.7.
- Use size, weight, and spacing to create hierarchy — not color alone.
- Keep line lengths 60–80 characters for comfortable reading.
- Avoid ultra-light weights for body text; they reduce legibility.

---

### 5. MODEST
**Let the content speak. The design should not show off.**

- Ask: *Does this page feel like it's trying to impress the designer's skills or help the user?*
- Modesty means choosing the understated option when two choices are equally functional.
- Parallax scrolling, 3D transforms, complex entrance animations — these are "look at me" choices, not user-first choices.

**Design guidance:**
- Reduce or remove motion and animations unless they communicate something (e.g., loading state, transition context).
- Avoid gradient hero sections, glassmorphism, and other "current trend" aesthetics that will date the design.
- Choose plain background colors over complex texture or pattern.

---

### 6. TIMELESS
**Design for longevity, not the current trend.**

- Ask: *Will this design feel dated in 2 years?*
- Trends (glassmorphism, neumorphism, bento grids, dark-mode-everything) age quickly.
- Timeless design uses proven patterns: clear nav, readable type, logical layout.
- The Drudge Report has run on the same design for decades and serves millions of readers.

**Design guidance:**
- Avoid relying on a specific CSS trend for visual interest.
- Prioritize layout clarity and information architecture over visual novelty.
- Use standard UI patterns (hamburger menu, sticky nav, card grid) — they work because users already know them.

---

### 7. MATERIALLY HONEST
**Don't make flat things look 3D, or fake materials you're not using.**

- Ask: *Does any visual element imply a physical property the interface doesn't have?*
- This is about integrity: buttons should look like buttons; links should look like links.
- Fake shadows, embossing effects, and faux-leather textures are materially dishonest.

**Design guidance:**
- Ensure interactive elements look interactive (affordance).
- Don't use visual tricks that confuse whether something is clickable or decorative.
- Flat design is fine — just make sure clickable things *look* different from non-clickable ones.

---

### 8. EASY TO IMPLEMENT
**If a design is too complex to build, it won't be built well.**

- Ask: *Can a solo developer or small team maintain this design without major effort?*
- Complexity in design creates complexity in code, which creates bugs and technical debt.
- The best designs are often simple enough to be built in plain HTML and CSS.

**Design guidance:**
- Prefer CSS Grid and Flexbox layouts over overly complex absolute-positioning.
- Avoid designs that require heavy JavaScript for layout or animation.
- Design with a component system in mind — consistent spacing, color tokens, reusable patterns.

---

### 9. COMMERCIALLY VALUABLE
**Simplicity sells. Complexity distracts from conversion.**

- Ask: *Does this design make it easy for users to do the thing that generates business value?*
- The "story" (your value proposition in words) matters more than visual polish.
- Clutter on a landing page competes with the CTA (call to action).

**Design guidance:**
- Ensure the primary CTA is immediately visible above the fold.
- Reduce the number of competing CTAs — one main action per page section.
- Lead with a clear, plain-language headline that states what you do and for whom.
- Remove unnecessary marketing content (stock photos of smiling people, generic taglines).

---

### 10. PERFORMANT
**A fast page is a better page. Performance is UX.**

- Ask: *How quickly does this page load on a slow mobile connection?*
- Every additional script, image, and font has a performance cost.
- Slow load times increase bounce rate and reduce trust.

**Design guidance:**
- Use system fonts or limit web font files to 1–2 weights.
- Compress and lazy-load images; use modern formats (WebP, AVIF).
- Avoid loading third-party tracking/analytics scripts that aren't essential.
- Minimize use of heavy JavaScript frameworks when simpler HTML/CSS will do.

---

### 11. ACCESSIBLE
**A design that excludes users has failed.**

- Ask: *Can this interface be used by someone with low vision, motor impairment, or using a screen reader?*
- Accessibility is also good SEO and good legal practice.

**Design guidance:**
- Maintain a contrast ratio of at least 4.5:1 for body text (WCAG AA).
- All interactive elements must be keyboard-navigable with visible focus states.
- Images must have descriptive `alt` text.
- Don't rely on color alone to communicate meaning (use shape, icon, or text too).
- Ensure tap targets are at least 44x44px on mobile.

---

### 12. FOCUSED
**Each page should have one primary purpose.**

- Ask: *What is this page trying to accomplish? Is everything on it serving that goal?*
- A page that tries to do everything does nothing well.
- Focus reduces decision fatigue for users.

**Design guidance:**
- Define a single primary action per page (sign up, read article, view product).
- Remove secondary navigation or content that pulls users away from the primary goal.
- Use progressive disclosure: show more detail only when the user requests it.

---

### 13. CLEAR
**If users have to think about how to use the interface, it's not clear enough.**

- Ask: *Where does the user's eye go first? Is that where it should go?*
- Clarity is about reducing ambiguity: users should never wonder "what does this button do?" or "where am I?"

**Design guidance:**
- Use visual hierarchy to direct attention: largest/boldest = most important.
- Show the user where they are (breadcrumbs, active nav states, progress indicators).
- Error messages should explain what went wrong and what to do next — not just "error."
- Don't use jargon. Use the words your users use.

---

### 14. DISTRACTION FREE
**Remove everything that pulls attention away from the user's goal.**

- Ask: *What on this page could distract a user from completing their primary task?*
- Autoplay video, pop-up subscriptions, sticky banners, and social share bars are all attention thieves.

**Design guidance:**
- Disable autoplay for video and audio.
- Delay or eliminate email capture pop-ups.
- Don't show social follower counts unless they add credibility in context.
- Remove sidebars unless they add navigation value (most don't).

---

### 15. PRODUCTIVE
**The interface should help users accomplish their goals efficiently.**

- Ask: *How many steps does it take for a user to do what they came here to do?*
- Every extra click, form field, or page load is friction.

**Design guidance:**
- Streamline forms: request only required information; use smart defaults.
- Provide search functionality if the site has significant content depth.
- Use persistent navigation for frequently accessed areas.
- Remember user preferences where appropriate (filters, settings, last viewed).

---

## How to Apply This Skill

### When Reviewing a Design
1. Identify which principles are being violated (most pages violate 3–6).
2. Prioritize the top 3 issues by impact on user clarity and conversion.
3. Provide specific, actionable fixes — not just "make it simpler."

### When Designing from Scratch
1. Start with words and structure before visuals.
2. Default to system fonts, simple layout, and black text on white.
3. Add visual complexity only when it serves comprehension.

### Scoring a Design (optional)
Rate each principle 1–3:
- **1** = Actively violated
- **2** = Neutral / not addressed
- **3** = Well executed

Total: /45. A score above 35 is a solid simple design.

---

## Quick Reference Checklist

```
☐ Content-element ratio is high (content dominates)
☐ All UI elements are clearly labeled in words
☐ No elements present that don't serve the user
☐ Strong typographic hierarchy with readable body text
☐ No trend-based aesthetics that will date the design
☐ Interactive elements look interactive
☐ Primary CTA is visible without scrolling
☐ Page loads fast (< 2s on broadband)
☐ Passes WCAG AA contrast check
☐ Each page has one clear purpose
☐ User's eye is guided to the most important thing first
☐ No distracting elements (autoplay, pop-ups, sidebars)
☐ Task completion requires minimum steps
```

---

*Based on Anthony Hobday's "Simple Web Design" — https://anthonyhobday.com/books/simpledesign/*
