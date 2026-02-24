# simple-web-design

> An agent skill for auditing, critiquing, and building better websites — grounded in Anthony Hobday's 15 principles of simple web design.

Install with:
```bash
npx skills add <your-github-username>/simple-web-design
```

---

## What it does

This skill teaches your AI agent to apply **15 battle-tested web design principles** whenever you ask for:

- Design feedback on a website, landing page, or app
- A UX or UI audit
- Help designing a web page from scratch
- A code review of frontend/UI code

The skill is grounded in Anthony Hobday's book [*Simple Web Design*](https://anthonyhobday.com/books/simpledesign/) — a practical, opinionated framework that prioritizes **content, clarity, and longevity** over visual complexity and trend-chasing.

---

## The 15 Principles

| Principle | Focus |
|-----------|-------|
| Content First | Design serves content, not the other way around |
| Wordy | Words are a design material; label everything |
| Minimal | Every element must earn its place |
| Typographic | Typography is the primary design tool |
| Modest | The design shouldn't show off |
| Timeless | Avoid trends; design for longevity |
| Materially Honest | Clickable things should look clickable |
| Easy to Implement | Complexity in design = complexity in code |
| Commercially Valuable | Simplicity converts; clutter distracts |
| Performant | A fast page is a better page |
| Accessible | Design that excludes users has failed |
| Focused | Each page should have one purpose |
| Clear | Visual hierarchy guides the eye |
| Distraction Free | Remove anything competing with the user's goal |
| Productive | Fewer steps = higher completion |

---

## What's inside

```
simple-web-design/
├── SKILL.md                    # Core skill: principles summary + quick audit checklist
└── references/
    ├── principles.md           # Deep breakdown of all 15 principles with code examples
    └── audit-guide.md          # Structured audit workflow, by site type, for clients/teams
```

The skill uses **progressive disclosure** — the agent loads reference files only when needed, keeping context usage lean for quick checks.

---

## Example prompts

- *"Review my landing page at [URL] and tell me what's wrong with the UX"*
- *"I'm building a SaaS onboarding flow — help me design it simply"*
- *"Here's my homepage code — flag anything that violates good web design principles"*
- *"Score my site's design and give me the top 3 things to fix"*
- *"Is this Figma screenshot too cluttered?"*

---

## Based on

Anthony Hobday — [Simple Web Design](https://anthonyhobday.com/books/simpledesign/)

---

## License

MIT
