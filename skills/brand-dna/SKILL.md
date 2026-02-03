---
name: brand-dna
description: Build a complete Brand DNA framework from scratch. Use this skill when the user wants to define, document, or develop a brand identity, brand strategy, brand guidelines, brand DNA, brand architecture, brand personality, brand voice, or brand positioning. Supports guided workshop mode (step-by-step discovery), direct creation mode, brand audit mode, and multiple output formats including presentations and brand books.
---

# Brand DNA Framework

## Overview

This skill helps users create a comprehensive Brand DNA document — the foundational strategic framework that defines who a brand is, what it stands for, how it communicates, and how it shows up in the world.

**Keywords**: brand DNA, brand identity, brand strategy, brand guidelines, brand personality, brand voice, brand values, brand positioning, brand architecture, brand story, brand framework, brand book, brand audit, brand presentation

## Modes

### Mode 1: Guided Workshop

Use when the user wants help *discovering* their brand DNA through strategic questioning.

**Trigger phrases**: "help me figure out my brand", "I'm starting a new brand", "workshop my brand", "guide me through", "I don't know where to start"

**Process:**

1. **Read** the workshop questions from `references/workshop-questions.md`
2. **Present questions one section at a time** — do not dump all questions at once
3. **Start with Purpose & Origin**, then progress through each section sequentially
4. **Synthesize answers** into framework language after each section
5. **Reflect back** a summary of what you've captured before moving to the next section
6. **After all sections**, compile the full Brand DNA document
7. **Present the Post-Workshop Menu** (see below)

**Rules for workshop facilitation:**
- Ask 2-4 questions per turn, grouped by theme
- Acknowledge and build on the user's answers before asking the next set
- Offer examples or prompts when the user is stuck
- If the user gives short answers, probe deeper with follow-ups
- Let the user skip sections they aren't ready for — circle back later

### Mode 2: Direct Creation

Use when the user already has brand information and wants it structured into the framework.

**Trigger phrases**: "here's my brand info", "structure this into a brand DNA", "format my brand guidelines", "I already know my brand"

**Process:**

1. **Gather** whatever brand information the user provides
2. **Map** their input to the framework components (see `references/framework-components.md`)
3. **Identify gaps** — flag any missing framework components and ask if the user wants to fill them
4. **Generate** the complete Brand DNA document in markdown
5. **Present the Post-Workshop Menu** (see below)

### Mode 3: Brand Audit

Use when the user wants to evaluate existing brand materials against the framework.

**Trigger phrases**: "audit my brand", "brand health check", "evaluate my brand", "assess my brand", "review my brand materials"

**Process:**

1. **Read** the audit rubric from `references/audit-rubric.md`
2. **Request materials** — ask the user to share existing brand documents, website copy, social posts, and guidelines
3. **Score each component** (1-5) using the rubric criteria
4. **Calculate overall brand health score** using the weighted formula
5. **Generate audit report** with:
   - Component scores and ratings
   - Identified strengths
   - Critical gaps (scores 1-2)
   - Quick wins (scores 3)
   - Prioritized recommendations
6. **Offer mini-workshops** for weak components using targeted questions from `references/workshop-questions.md`

### Mode 4: Voice Sample Generator

Use when the user wants to see their brand voice in action across multiple contexts.

**Trigger phrases**: "generate voice samples", "show me voice examples", "what does my brand sound like", "voice in action"

**Prerequisite:** Requires a completed Brand DNA (at minimum: voice, personality, and values sections).

**Process:**

1. **Read** the voice contexts from `references/voice-contexts.md`
2. **Generate 10 voice samples** across all defined contexts:
   - Homepage headline
   - Error message
   - Social post (celebratory)
   - Social post (announcement)
   - Email subject line
   - Push notification
   - About page opener
   - Support response (positive)
   - Support response (negative)
   - Internal Slack message
3. **Explain each sample** — show how it reflects the brand voice
4. **Summarize voice principles** demonstrated across samples

### Mode 5: Competitive Positioning Helper

Use when the user wants deep analysis of their competitive landscape and positioning options.

**Trigger phrases**: "competitive positioning", "analyze competitors", "differentiation", "positioning options", "competitive landscape"

**Process:**

1. **Gather competitor information** — ask user to provide 2-4 competitors
2. **Analyze each competitor** on:
   - Apparent positioning and audience
   - Brand personality and voice
   - Strengths and weaknesses
   - Messaging and differentiation claims
3. **Map the competitive landscape** — identify patterns and clusters
4. **Identify white space** — opportunities for differentiation
5. **Draft 2-3 positioning statement options** with rationale for each
6. **Recommend preferred positioning** with justification

---

## Post-Workshop Menu

After completing a Brand DNA document (via Mode 1 or Mode 2), automatically present this menu:

```
Your Brand DNA is complete! What would you like to create next?

1. 📊 Stakeholder presentation (PPTX) — 10-12 slides for team or investors
2. 📄 One-page executive summary — Condensed Brand DNA for quick reference
3. 📕 PDF brand book — Comprehensive document with extended examples
4. 📱 Social media bios — Platform-specific copy for Twitter, LinkedIn, Instagram, TikTok
5. 🎤 Voice samples — See your brand voice across 10 different contexts
6. 🏁 Export and finish — Take your Brand DNA document and go

You can choose multiple options or type "done" to finish.
```

**Handling selections:**

- **Option 1 (Presentation):** Invoke `document-skills:pptx` using `references/presentation-template.md`
- **Option 2 (Executive Summary):** Generate one-page summary (see Output Formats below)
- **Option 3 (PDF Brand Book):** Invoke `document-skills:pdf` with comprehensive content
- **Option 4 (Social Bios):** Generate platform-specific bios (see Output Formats below)
- **Option 5 (Voice Samples):** Enter Mode 4 (Voice Sample Generator)
- **Option 6 (Export):** Confirm completion and offer the markdown document

Allow users to select multiple options in sequence.

---

## Output Formats

### Primary Output: Brand DNA Document

Always output the Brand DNA as a structured markdown document using this skeleton:

```markdown
# [Brand Name] — Brand DNA

## Purpose
Why does this brand exist beyond making money?

## Vision
What future is this brand working toward?

## Mission
What does this brand do, for whom, and how?

## Core Values
3-5 non-negotiable principles that guide every decision.

## Brand Personality
The human traits this brand embodies. Define the archetype and 3-5 personality adjectives.

## Brand Voice & Tone
How the brand sounds across all communication.
- **Voice** (constant): [e.g., confident, warm, direct]
- **Tone spectrum** (contextual): [e.g., formal ↔ casual, serious ↔ playful]
- **Language principles**: Do's and Don'ts for word choice, sentence style, and rhetoric.

## Positioning
- **Target audience**: Who this brand serves (demographics + psychographics)
- **Category**: The market space the brand operates in
- **Differentiation**: What makes this brand the only ___ that ___
- **Positioning statement**: For [audience], [Brand] is the [category] that [key benefit] because [reason to believe].

## Brand Story
The narrative arc — origin, struggle, breakthrough, and where it's headed.

## Visual Identity Direction
High-level guidance on the visual world of the brand (not a design spec, but strategic direction).
- **Color mood**: [e.g., earthy and warm / bold and electric / muted and minimal]
- **Typography feel**: [e.g., modern sans-serif / classic serif / hand-drawn]
- **Imagery style**: [e.g., candid photography / flat illustration / textured collage]
- **Overall aesthetic**: [1-2 sentence description]

## Tagline / Mantra
A memorable phrase that captures the brand's essence. Provide 3-5 options.

## Brand Do's and Don'ts
Concrete behavioral guidelines for anyone representing the brand.
```

### Stakeholder Presentation (PPTX)

Invoke `document-skills:pptx` with the Brand DNA and presentation template.

**Slide structure** (see `references/presentation-template.md`):

| # | Slide | Content Source |
|---|-------|----------------|
| 1 | Title | Brand name + tagline |
| 2 | The Problem | Audience pain points |
| 3 | Purpose | Why we exist |
| 4 | Vision & Mission | Future + present action |
| 5 | Core Values | 3-5 values |
| 6 | Personality | Archetype + adjectives |
| 7 | Voice | How we sound + examples |
| 8 | Positioning | Differentiation + statement |
| 9 | Story | Narrative arc |
| 10 | Visual Direction | Color/type/imagery mood |
| 11 | Do's & Don'ts | Key guidelines |
| 12 | Summary | Tagline options + CTA |

**Invocation:**
```
Create a stakeholder presentation for [Brand Name] using the completed Brand DNA.
Follow the slide structure in the Brand DNA Presentation Template.
Include speaker notes for each slide.
Apply visual styling consistent with the Visual Identity Direction.
```

### One-Page Executive Summary

Generate a condensed Brand DNA for quick reference:

```markdown
# [Brand Name] — Executive Summary

## Essence
[Purpose, vision, and mission distilled into 3 sentences]

## Identity
- **Values:** [3-5 values as bullet points]
- **Personality:** [Archetype + 3 adjectives]
- **Voice:** [2-3 key voice characteristics]

## Position
**For** [target audience], **[Brand]** is the [category] that [key benefit] because [reason to believe].

## Tagline
[Primary tagline option]

---
*Full Brand DNA available upon request.*
```

### PDF Brand Book

Invoke `document-skills:pdf` to create a comprehensive brand document.

**Structure:**
1. Cover page (brand name, tagline, "Brand Guidelines")
2. Table of contents
3. All 11 Brand DNA sections (full content)
4. Extended voice examples (5+ samples across contexts)
5. Do's and Don'ts reference card (formatted for printing)
6. Contact/ownership information

**Invocation:**
```
Create a comprehensive PDF brand book for [Brand Name] using the completed Brand DNA.
Include a cover page, table of contents, all framework sections, extended voice examples, and a Do's/Don'ts reference card.
```

### Social Media Bios

Generate platform-specific copy:

```markdown
## Social Media Bios: [Brand Name]

### Twitter/X (160 characters max)
[Bio text — punchy, personality-forward, may include emoji if on-brand]

### LinkedIn (2000 characters max)
[Bio text — more professional, can include mission/values, calls to action]

### Instagram (150 characters max)
[Bio text — visual-first audience, personality-forward, emoji acceptable]

### TikTok (80 characters max)
[Bio text — ultra-concise, casual, trend-aware if on-brand]

---

**Usage notes:**
- Adapt handles and links per platform
- Update seasonally or with major brand changes
- Maintain consistent profile imagery across platforms
```

### Voice Samples

Generate using Mode 4 process and `references/voice-contexts.md`.

### Audit Report

Generate using Mode 3 process and `references/audit-rubric.md`.

---

## Quality Standards

When generating a Brand DNA document:

- **Be specific, not generic.** "We value innovation" is useless. "We ship the scrappy version first and refine in public" is a brand value.
- **Use the brand's own language.** Mirror the vocabulary, rhythm, and energy the user has expressed.
- **Differentiate or delete.** Every element should distinguish this brand from competitors. If a value or trait could apply to any company in the category, sharpen it.
- **Show tension.** Great brands have a point of view that *excludes* some people. Don't water it down.
- **Voice examples matter.** For Brand Voice & Tone, always include 2-3 example sentences showing the voice in action (e.g., a social post, an error message, a headline).
- **Positioning is a strategy, not a slogan.** The positioning statement should be analytically precise, not marketing copy.

## Handling Partial Input

If the user provides incomplete information:

1. Generate what you can with confidence
2. Mark uncertain sections with `[NEEDS INPUT]` placeholders
3. List the specific questions needed to complete those sections
4. Offer to run a mini-workshop for just the missing pieces

---

## Cross-Skill Invocations

This skill integrates with other document skills:

| Output | Skill | Invocation Pattern |
|--------|-------|-------------------|
| Presentation | `document-skills:pptx` | Pass Brand DNA + presentation template |
| PDF Brand Book | `document-skills:pdf` | Pass Brand DNA + book structure |
| Voice Samples | Internal (Mode 4) | Use `references/voice-contexts.md` |
| Audit Report | Internal (Mode 3) | Use `references/audit-rubric.md` |

---

## References

- `references/framework-components.md` — Detailed definitions and examples for each Brand DNA component
- `references/workshop-questions.md` — Full question bank for guided brand discovery
- `references/presentation-template.md` — Slide structure and guidelines for stakeholder presentations
- `references/audit-rubric.md` — Scoring criteria for brand health assessment
- `references/voice-contexts.md` — 10 contexts for voice sample generation
