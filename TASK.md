# Task: Build AI Showcase Page

Create a new HTML page called `ai-showcase.html` in this directory. This page is for the 123-ai.co.uk website — an AI consulting firm for small UK businesses with a "Work From Walk" / nature ethos.

## Purpose

Showcase that this entire website was designed, built and deployed by an AI agent — demonstrating 123-AI's capability to rapidly deliver real, polished digital work. It should be compelling, honest, and on-brand.

## Design Requirements

Must match the existing site exactly. Copy the full CSS from index.html into ai-showcase.html. Use the same:
- CSS custom properties (--forest, --canopy, --moss, --fern, --mist, --cream, --warm-white, --gold, etc.)
- Font stack: Playfair Display (display) + Lato (body) via Google Fonts
- Same nav as index.html (copy it exactly, add "AI Showcase" as active link)
- Same footer as index.html (copy it exactly)
- Same button classes (.btn, .btn-primary, .btn-cream, .btn-lg, .btn-outline)
- Same section patterns (.section-label, .section-title, .section-intro)

## Page Sections

### 1. Hero
Bold headline: "This website was built by an AI agent."
Subheadline: A single AI agent, given a brief, designed and shipped a complete professional website — from blank canvas to live URL — without a human writing a single line of code.
CTA button: "Book a Free Call" → mailto:hello@123-ai.co.uk

### 2. The Story (vertical timeline)
How it was built — each step as a timeline item with icon + title + short copy:
- 🎯 Brief Received — A plain-English description of the business and what the site needed to achieve
- 🤔 Requirements Explored — The agent analysed the brief, asked clarifying questions, and proposed a structure
- 🎨 Design System Chosen — Nature palette (forest greens, cream, gold), Playfair Display for headings, Lato for body
- ✍️ Pages Written — Home, Blog, and supporting pages structured and written from scratch
- 🖼️ Images Sourced — Hero backgrounds and section images selected and optimised
- 🚀 Committed & Deployed — Code pushed to GitHub, live on GitHub Pages via custom domain

### 3. By the Numbers (stats grid, 2x3 or 3x2)
- 5 — Pages created
- ~3,000 — Lines of HTML & CSS written
- 0 — Human coders involved
- < 2 hrs — From brief to live website
- 1 — AI agent
- £0 — In development fees

### 4. What This Means For You
Bridge section: If an AI agent can build a polished, production-ready website this quickly — what could it do for your back-office workflows, customer communications, or data management? This is exactly the kind of speed and quality we bring to every client engagement.
CTA: "See What AI Can Do For Your Business" → #contact

### 5. FAQ (2-column grid, same style as index.html)
Three questions:
1. "Did a human design this?" — The brief and creative direction came from a human. Every word, every line of code, and every design decision was made by an AI agent. That's not a disclaimer — it's the point.
2. "Can AI do this for my business?" — Yes, and it goes much further. Websites are just the start. AI agents today can handle client communications, data processing, document generation, scheduling and more — all at the same speed.
3. "Is this just a gimmick?" — No. This page exists because the question "how good is AI really?" deserves a live answer, not a sales pitch. You're looking at it.

### 6. Bottom CTA Box
Same as index.html bottom CTA — dark green gradient box with "Ready to reclaim your afternoons?" headline and email CTA.

## Nav Updates Required

Also update these two files to add "AI Showcase" to the navigation:

**index.html** — find this line:
```
<li><a href="blog.html">Blog</a></li>
```
And add BEFORE it:
```
<li><a href="ai-showcase.html">AI Showcase</a></li>
```

**blog.html** — same change: add the AI Showcase nav link before the Blog link.

## Tone

Confident, honest, slightly playful. Not boastful — the page itself is the proof. Write in the same voice as the rest of the site. No corporate fluff.

## After Building

1. git add -A
2. git commit -m "Add AI Showcase page demonstrating agent-built website"
3. git push origin main
4. Run: openclaw system event --text "Done: AI Showcase page built, committed and pushed to GitHub" --mode now
