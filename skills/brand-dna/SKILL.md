---
name: brand-dna
description: Build a complete Brand DNA framework from scratch. Use this skill when the user wants to define, document, or develop a brand identity, brand strategy, brand guidelines, brand DNA, brand architecture, brand personality, brand voice, or brand positioning. Supports both a guided workshop mode (step-by-step discovery) and a direct creation mode.
---

# Brand DNA Framework

## Overview

This skill helps users create a comprehensive Brand DNA document — the foundational strategic framework that defines who a brand is, what it stands for, how it communicates, and how it shows up in the world.

**Keywords**: brand DNA, brand identity, brand strategy, brand guidelines, brand personality, brand voice, brand values, brand positioning, brand architecture, brand story, brand framework, brand book

## Modes

### 1. Guided Workshop Mode

Use when the user wants help *discovering* their brand DNA through strategic questioning.

**Trigger phrases**: "help me figure out my brand", "I'm starting a new brand", "workshop my brand", "guide me through", "I don't know where to start"

**Process:**

1. **Read** the workshop questions from `references/workshop-questions.md`
2. **Present questions one section at a time** — do not dump all questions at once
3. **Start with Purpose & Origin**, then progress through each section sequentially
4. **Synthesize answers** into framework language after each section
5. **Reflect back** a summary of what you've captured before moving to the next section
6. **After all sections**, compile the full Brand DNA document

**Rules for workshop facilitation:**
- Ask 2-4 questions per turn, grouped by theme
- Acknowledge and build on the user's answers before asking the next set
- Offer examples or prompts when the user is stuck
- If the user gives short answers, probe deeper with follow-ups
- Let the user skip sections they aren't ready for — circle back later

### 2. Direct Creation Mode

Use when the user already has brand information and wants it structured into the framework.

**Trigger phrases**: "here's my brand info", "structure this into a brand DNA", "format my brand guidelines", "I already know my brand"

**Process:**

1. **Gather** whatever brand information the user provides
2. **Map** their input to the framework components (see `references/framework-components.md`)
3. **Identify gaps** — flag any missing framework components and ask if the user wants to fill them
4. **Generate** the complete Brand DNA document in markdown

## Output Format

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

## References

- `references/framework-components.md` — Detailed definitions and examples for each Brand DNA component
- `references/workshop-questions.md` — Full question bank for guided brand discovery
