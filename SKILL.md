---
name: simple-web-design
description: >
  Apply proven simple web design principles to critique, audit, improve, or build website UI and
  UX. Trigger this skill whenever a user asks for design feedback, a UX review, landing page
  critique, or help designing any web interface — even when phrased casually as "does this look
  good?", "what's wrong with my site?", "how do I improve UX?", "review my homepage", "make my
  app feel cleaner", or "help me design a page". Also trigger when a user shares a URL, a
  screenshot, or code and wants design input, or asks to review frontend/UI code for design
  quality. This skill is grounded in Anthony Hobday's "Simple Web Design" framework: 15
  battle-tested principles that prioritize content, clarity, and long-term usability over visual
  complexity and trend-chasing.
---

# Simple Web Design

A framework for auditing, critiquing, and building better websites — grounded in Anthony Hobday's
15 principles of simple web design. Applicable to landing pages, SaaS products, portfolios,
e-commerce, dashboards, and any digital interface.

> **Core philosophy**: Good content has more impact than the rest of the design. The design's job is to get out of the way.

---

## The 15 Principles

### 1. Content First
Design serves content — not the other way around. Content is whatever the user came to see.
Measure the **content-element ratio**: meaningful content vs. decorative/structural elements. High ratio = respect for the user.
- Remove decorative imagery, gradients, and animations that don't make content clearer
- Ask: "If I removed this, would the user miss it?" If no → remove it
- Violations: full-screen hero photos pushing content below the fold, stock images of smiling people, splash screens

### 2. Wordy
Words are a design material — often the most powerful one. Don't cut words to look minimal; cut words that don't add meaning.
- Label every interactive element with a verb phrase: "Download report", "Add team member"
- If a tooltip explains what a button does, that text should be the button label
- Violations: icon-only navigation, buttons labeled "Go →" or "Submit", marketing copy that sounds impressive but explains nothing

### 3. Minimal
Every element increases cognitive load. Minimalism is functional restraint, not visual sparseness.
- Apply the "earn your place" test: every element must justify its existence
- Audit nav links, feature lists, sidebar widgets, pop-ups — remove what isn't used
- Violations: 8-item navigation, 20-feature grids, simultaneous cookie banners + chat bubbles + newsletter pop-ups

### 4. Typographic
Typography is the primary design tool of the web. A well-typeset page needs no decoration.
- Body text ≥ 16px, line-height 1.5–1.7, max line length 60–80 characters
- Max 2 typefaces, max 3 weights; hierarchy via size/weight — not color alone
- Violations: 14px body text, ultra-light weights, 4+ typefaces, full-width text on desktop

### 5. Modest
The design should not show off. Choose the understated option when two choices are equally functional.
- Motion should communicate state (loading, transition) — not decorate
- Remove animations that don't help users understand what happened or what's next
- Violations: scroll-triggered animations on every section, glassmorphism, parallax, cursor follower effects

### 6. Timeless
Design for longevity, not the current trend. Trend-based design ages quickly and creates redesign debt.
- Rely on proven patterns: clear nav, readable type, logical layout, black + white + one accent
- Avoid committing to: bento grids, gradient text headers, bubbly SaaS illustration styles
- The Drudge Report has served millions for decades on the same design — functional clarity outlasts fashion

### 7. Materially Honest
Elements should accurately communicate their interactive nature. Don't fake affordances you don't have; don't hide ones you do.
- Interactive elements need consistent visual treatment (color/border for buttons, underline/color for links)
- Non-interactive elements should look inert — no hover cursor, no border implying a card
- Violations: buttons that look like plain text, links indistinguishable from body copy, decorative cards that look clickable

### 8. Easy to Implement
Design complexity compounds into code complexity: edge cases, bugs, performance regressions.
- Prefer CSS Grid/Flexbox over absolute positioning; standard breakpoints over pixel-perfect custom layouts
- Design for the developer maintaining this in 2 years
- Violations: canvas animations for backgrounds, irregular masonry layouts, JS-dependent layout logic

### 9. Commercially Valuable
Simplicity converts. Clutter competes with the action you want users to take.
- Primary CTA visible above the fold, visually dominant; one primary CTA per page section
- Hero headline: 8–12 words, plain language, states who this is for and what they get
- Violations: 4 competing CTAs above the fold, clever headlines that don't explain the product, generic testimonials

### 10. Performant
A fast page is a better page. Performance is UX. Every asset, script, and font has a cost.
- Targets: LCP < 2.5s, page weight < 1MB for landing pages, max 2 web font families
- Compress and lazy-load images; use WebP/AVIF; audit third-party scripts ruthlessly
- Violations: uncompressed hero images, 4+ font families, a dozen analytics/tracking scripts

### 11. Accessible
Design that excludes users has failed. Accessibility is also good SEO and good legal practice.
- Text contrast ≥ 4.5:1 (WCAG AA); tap targets ≥ 44×44px; keyboard navigation with visible focus states
- Color must not be the sole way to communicate meaning; all images need descriptive alt text
- Violations: `outline: none` on focus, gray text on white below 4.5:1, icon buttons without aria-label

### 12. Focused
Each page should have one primary purpose. A page that tries to do everything does nothing well.
- Define one primary action per page before designing anything; secondary actions visually subordinate
- Use progressive disclosure: summary → detail, not everything at once
- Violations: landing page that's also a blog index and product tour, 15 "start here" entry points on a dashboard

### 13. Clear
If users have to think about how to use the interface, it's not clear enough.
- Visual hierarchy directs attention: largest/boldest = most important; show location with active nav states
- Error messages: [what went wrong] + [what to do] — not just "Something went wrong"
- Violations: navigation with jargon labels, ambiguous button placement, no feedback on form submission

### 14. Distraction Free
Remove everything that competes with the user's goal. Each distraction costs cognitive resources.
- Delay optional pop-ups until the user signals engagement (80% scroll or 60s dwell)
- Live chat: hide on mobile, delay on desktop; social share widgets belong at bottom, not mid-article
- Violations: autoplay video, newsletter pop-up on page load, sticky banners covering 40% of viewport

### 15. Productive
Help users accomplish their goals in as few steps as possible. Every extra click is friction.
- Streamline forms: only required fields; smart defaults; remember previous choices
- Consider "try before you sign up" flows — let users experience value first
- Violations: account required before any product value, 7-field contact forms, settings buried 3 levels deep

---

## Example Prompts

**Audit a live site**
> "Review https://example.com and score it against the 15 simple design principles. Give me the top 3 violations with specific fixes."

**Score a page**
> "Score my landing page at [URL] on all 15 principles from 1–3. Give me a total out of 45 and prioritize the worst issues."

**Audit a screenshot or Figma**
> "Here's a screenshot of my homepage. Audit it for visual clutter and tell me what's competing with the main CTA."

**Code review**
> "Review this HTML/CSS and flag anything that violates simple web design principles: [paste code]"

**Build from scratch**
> "Help me design a simple SaaS pricing page. Start with the content structure, then suggest the layout."

**Single principle**
> "Is my navigation too cluttered? Apply the Minimal and Focused principles and tell me what to cut."

**Override**
> "My brand requires a trend-forward style — I can't change that. Apply the other 14 principles to improve everything else."

---

## Programmatic Usage

This skill activates through natural language — no special API parameters required. Pass the user's design request directly to any compatible AI agent. The skill loads automatically when the request matches design feedback, audit, or UX patterns.

**Claude API — audit a URL:**
```javascript
import Anthropic from "@anthropic-ai/sdk";
const client = new Anthropic();

const response = await client.messages.create({
  model: "claude-opus-4-5",
  max_tokens: 1024,
  messages: [{
    role: "user",
    content: "Review https://example.com and score it against the 15 simple design principles. Give me the top 3 violations with specific fixes."
  }]
});
console.log(response.content[0].text);
```

**Claude API — code review:**
```javascript
const response = await client.messages.create({
  model: "claude-opus-4-5",
  max_tokens: 1024,
  messages: [{
    role: "user",
    content: `Review this HTML and flag any simple web design principle violations:\n${yourCode}`
  }]
});
```

**Expected audit response format:**
```
[Principle #N — Name] Score: X/3
Problem: specific description of the violation
Fix: concrete actionable recommendation

Total: XX/45
Priority fixes: [ordered by impact]
```

---

## Working with Exceptions

When a project has legitimate constraints that conflict with a principle, use this process:

1. **Name the exception explicitly** — state which principle is being overridden and why
   - *"Overriding #6 Timeless — brand requires trend-forward visuals"*

2. **Apply all remaining principles at full strength** — an exception to one never justifies relaxing others

3. **Contain the exception** — limit it to the specific element that needs it, not the whole design

4. **Flag it in audit output** so future reviewers know it was intentional
   - *"Note: #6 Timeless intentionally overridden for brand alignment"*

**Common legitimate exceptions:**
| Constraint | Principle overridden | What to enforce instead |
|---|---|---|
| Brand requires trend-forward visuals | #6 Timeless | All 14 others at full strength |
| Legal requires dense fine print | #3 Minimal | Make fine print as readable as possible (#4) |
| Marketing requires multiple CTAs | #12 Focused | Clear visual hierarchy between them (#13) |
| Complex product requires long onboarding | #15 Productive | Minimize steps within each stage |

---

## Context Management

This skill uses **progressive disclosure** to manage context efficiently:

**Always in context** (this file — SKILL.md):
- All 15 principles as compact summaries with violations and guidance
- Example prompts, quick checklist, scoring rubric
- Programmatic usage examples, exception handling

**Load on demand** — read these reference files when needed:

- **`references/principles.md`** — Deep implementation guidance for all 15 principles: detailed code patterns (before/after), CSS examples, performance budgets, contrast requirements, form optimization patterns. Load this when giving in-depth critiques, designing from scratch, or when the user asks for implementation-level detail on any specific principle.

- **`references/audit-guide.md`** — Structured audit workflows by site type (landing page, SaaS, e-commerce, blog, portfolio), scoring rubric, and templates for presenting findings to clients or teams. Load this when the user requests a formal audit report or asks how to structure and present findings.

---

## How to Respond

### Design Audits
1. Identify violated principles (most pages violate 3–6)
2. Prioritize by impact: conversion first, then clarity, then accessibility
3. Give specific, actionable fixes — not vague "simplify this"
4. For structured audits with scoring, read `references/audit-guide.md`

### Code Reviews
Flag anti-patterns by principle and use this format:
```
[Principle #N — Name]
Problem: what the code does wrong
Fix: the corrected snippet or approach
```

Common code violations:
| Anti-pattern | Principle |
|---|---|
| `<button><img src="icon.svg"></button>` with no label | #2 Wordy + #11 Accessible |
| `font-size: 13px` or `14px` for body text | #4 Typographic |
| `autoplay` on `<video>` | #14 Distraction Free |
| `outline: none` on `:focus` | #11 Accessible |
| Loading 4+ Google Font weights | #10 Performant |
| 3+ primary CTAs above the fold | #12 Focused + #9 Commercially Valuable |
| Placeholder-only `<input>` (no `<label>`) | #2 Wordy + #11 Accessible |

### Building from Scratch
1. Start with words and content structure — layout and visuals come last
2. Default to: system fonts, single-column layout, black on white
3. Add visual complexity only when it demonstrably helps comprehension

**Starter HTML structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page title — Site name</title>
</head>
<body>
  <header>
    <nav>
      <a href="/">Logo</a>
      <a href="/pricing">Pricing</a>
      <a href="/login">Sign in</a>
      <a href="/start" class="btn">Get started</a>
    </nav>
  </header>
  <main>
    <section class="hero">
      <h1>Clear value proposition for your specific audience</h1>
      <p>One sentence expanding on the headline.</p>
      <a href="/start" class="btn-primary">Primary action</a>
    </section>
  </main>
</body>
</html>
```

**Starter CSS (typographic foundation):**
```css
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: system-ui, -apple-system, sans-serif;
  font-size: 1.125rem;
  line-height: 1.65;
  color: #1a1a1a;
  background: #fff;
}

h1 { font-size: clamp(2rem, 5vw, 3.5rem); line-height: 1.1; font-weight: 700; }
h2 { font-size: clamp(1.5rem, 3vw, 2.25rem); line-height: 1.2; font-weight: 600; }

.container { max-width: 68ch; margin: 0 auto; padding: 0 1.5rem; }

.btn-primary {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: #1a1a1a;
  color: #fff;
  border-radius: 6px;
  font-weight: 600;
  text-decoration: none;
}
.btn-primary:hover { background: #333; }
.btn-primary:focus-visible { outline: 2px solid #1a1a1a; outline-offset: 3px; }
```

For principle-level implementation detail (code patterns, performance budgets, accessibility specifics), read `references/principles.md`.

---

## Quick Audit Checklist

```
CONTENT & CLARITY
☐ Content dominates — decorative elements are minimal
☐ Primary message clear within 5 seconds
☐ One primary CTA per page

TYPOGRAPHY
☐ Body text ≥ 16px, line-height 1.5–1.7, max 80 chars per line
☐ Max 2 typefaces, max 3 weights
☐ Hierarchy via size/weight, not color alone

INTERACTION
☐ Every interactive element looks interactive
☐ All buttons and links have clear text labels
☐ Keyboard navigation works; focus states visible

PERFORMANCE
☐ Page loads < 2s; images compressed and lazy-loaded
☐ Max 2 web font families

ACCESSIBILITY
☐ Text contrast ≥ 4.5:1 (WCAG AA)
☐ All images have alt text; tap targets ≥ 44×44px

COMMERCIAL
☐ Value proposition above the fold
☐ CTA is the most prominent element per section

DISTRACTION
☐ No autoplay, no immediate pop-ups
☐ Sidebar and widgets don't compete with primary content
```

---

## Scoring

Rate each of the 15 principles **1–3**:
- `1` = Actively violated
- `2` = Neutral / not addressed
- `3` = Well executed

**Total / 45:**
- 38–45: Excellent
- 28–37: Good — some friction worth addressing
- 18–27: Needs work — users are feeling the pain
- Below 18: Significant redesign needed

For structured audit workflows and how to present findings to clients or teams, read `references/audit-guide.md`.

---

*Based on Anthony Hobday's "Simple Web Design" — https://anthonyhobday.com/books/simpledesign/*
