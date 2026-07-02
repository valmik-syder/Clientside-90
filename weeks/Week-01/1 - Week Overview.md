## 🧱 Week 1 — HTML · CSS · Tailwind · Git · JavaScript Advanced

This is the foundation week. No React, no TypeScript, no frameworks doing the thinking for me — just raw HTML, CSS, Git, and JavaScript, built by hand so I actually understand what every layer is doing before I let a framework abstract it away.

### 🎯 Build Target: ClientSide.in Landing Page v0.1

A complete, responsive landing page for ClientSide — hero section, all 15 service cards with JS-based filtering, pricing tables, and a fully validated contact form. Built twice: once in pure HTML + CSS, then rebuilt in Tailwind — so I can actually compare what I'm replacing instead of just trusting the utility classes blindly. Deployed to GitHub Pages by end of week, target Lighthouse score 90+ across the board.

Before writing a single line of CSS, I spent 60 minutes in Figma sketching the layout — components, auto layout, design tokens. Skipping this step means refactoring the layout three times later. Doing it once, properly, up front.

---

### 📅 Day-by-Day

**Day 1 — Semantic HTML + Flexbox**
Built the full page layout from scratch. No Tailwind. Pure semantic HTML + CSS — hero with a flexbox nav, services row, footer. Validated with the W3C validator. Committed every section separately instead of one giant commit at the end.

**Day 2 — CSS Grid + Animations**
Added the services section using CSS Grid (`grid-template-areas`). Hover animations built with keyframes and transitions. Set up CSS custom properties to drive the entire color system, plus a dark mode toggle running purely off those variables.

**Day 3 — Tailwind Rebuild**
Rebuilt the entire layout in Tailwind only — deleted all the custom CSS. Ran both versions through Lighthouse side by side to compare scores and actually understand what Tailwind compiles down to, instead of treating it as magic.

**Day 4 — JavaScript, Part 1**
Added a live character counter (closures), an async form submit simulated with Promises, smooth scroll via `requestAnimationFrame`, and lazy image loading with `IntersectionObserver`.

**Day 5 — JavaScript, Part 2**
Added service card filtering using `filter`/`map`/`reduce` against a JSON array, URL-based filter state with `URLSearchParams`, and split everything into three proper ES6 modules instead of one big script file.

**Day 6 — Git + GitHub Mastery**
Set up full GitFlow — `main`, `develop`, and three feature branches. Practiced interactive rebase to squash commits, cherry-picked a commit across branches, enabled branch protection on `main`, and wrote a real README.

**Day 7 — Polish + Deploy**
Fixed every responsive breakpoint from 320px to 1440px. Chased down every remaining Lighthouse issue. Deployed to GitHub Pages — Day 1 of the portfolio, live.

---

### ✅ Depth Validation Checkpoint

Before calling Week 1 done, I need to be able to:

- Rebuild the Tailwind service card grid from memory in 20 minutes — no notes.
- Explain the JavaScript event loop (microtask queue vs. macrotask queue) without Googling it.
- Explain, in my own words, why flexbox was right for the nav and grid was right for the services section — not the other way around.

### ⚠️ Pitfalls I'm Watching For

- Not committing to Git after every meaningful change.
- Writing CSS without actually understanding each property in DevTools.
- Jumping to Tailwind before understanding what it's replacing.
- Skipping the Figma sketch and paying for it in layout rework later.

### 💼 Business Integration

Wrote my first ClientSide service offering description — 150 words, one service, the problem it solves, who it's for, and at what price. Going live as a service page paragraph on ClientSide.in.

