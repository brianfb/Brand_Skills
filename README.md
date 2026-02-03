# Brand Skills

A Claude Code plugin for strategic brand building. Includes the **Brand DNA Framework** skill — a structured approach to defining, discovering, documenting, and auditing brand identity.

## Installation

Install directly in Claude Code:

```
/install-plugin /path/to/Brand_Skills
```

Or install from GitHub:

```
/install-plugin https://github.com/brianbuschmann/Brand_Skills
```

---

## Quick Start

Once installed, trigger it by typing `/brand-dna` in Claude Code, or by naturally asking something that matches the skill's trigger phrases:

```
Help me figure out my brand
```

```
Workshop my brand identity with me
```

```
Audit my brand
```

Claude will guide you through a structured workshop to build your Brand DNA from scratch.

---

## Usage

### Mode 1: Guided Workshop

Best for: New brands or brands that need strategic clarity.

**Sample invocations:**

```
Help me figure out my brand
```

```
I'm starting a new brand and need help defining it
```

```
Workshop my brand identity with me
```

```
Guide me through creating a brand strategy
```

```
I don't know where to start with my brand
```

The workshop walks through 9 sections:
1. Purpose & Origin
2. Audience & Problem
3. Differentiation & Positioning
4. Values & Beliefs
5. Personality & Character
6. Voice & Communication
7. Brand Story
8. Visual & Sensory Direction
9. Tagline & Synthesis

---

### Mode 2: Direct Creation

Best for: Brands with existing information that needs structuring.

**Sample invocations:**

```
Here's my brand info, structure it into a Brand DNA:
- We're a sustainable coffee company
- Our audience is eco-conscious millennials
- We believe in transparency and fair trade
- Our voice is warm but direct
```

```
Format my existing brand guidelines into a Brand DNA framework
```

```
I already know my brand, just help me document it properly
```

```
Take this brand strategy deck and turn it into a structured Brand DNA
```

---

### Mode 3: Brand Audit

Best for: Existing brands that want to evaluate their strategic foundation.

**Sample invocations:**

```
Audit my brand
```

```
Do a brand health check for my company
```

```
Evaluate my brand against best practices
```

```
Assess my brand materials and tell me what's missing
```

```
Review my brand guidelines and score each component
```

Claude will ask for your existing materials (website, guidelines, social posts) and score each of the 11 Brand DNA components on a 1-5 scale, providing:
- Overall brand health score
- Strengths and critical gaps
- Prioritized recommendations
- Mini-workshop offers for weak areas

---

### Mode 4: Voice Sample Generator

Best for: Making brand voice tangible with real examples.

**Sample invocations:**

```
Generate voice samples for my brand
```

```
Show me what my brand sounds like across different contexts
```

```
Create voice examples for my Brand DNA
```

```
What does my brand voice sound like in action?
```

Generates 10 voice samples:
- Homepage headline
- Error message
- Social post (celebratory)
- Social post (announcement)
- Email subject line
- Push notification
- About page opener
- Support response (positive outcome)
- Support response (negative outcome)
- Internal Slack message

---

### Mode 5: Competitive Positioning Helper

Best for: Finding differentiation and white space in your market.

**Sample invocations:**

```
Help me with competitive positioning
```

```
Analyze my competitors and find differentiation opportunities
```

```
I need help positioning against [Competitor A], [Competitor B], and [Competitor C]
```

```
Map my competitive landscape and find white space
```

```
Give me positioning statement options based on my competitors
```

---

## Output Formats

After completing your Brand DNA, you'll see a menu of output options:

```
Your Brand DNA is complete! What would you like to create next?

1. Stakeholder presentation (PPTX) — 10-12 slides for team or investors
2. One-page executive summary — Condensed Brand DNA for quick reference
3. PDF brand book — Comprehensive document with extended examples
4. Social media bios — Platform-specific copy for Twitter, LinkedIn, Instagram, TikTok
5. Voice samples — See your brand voice across 10 different contexts
6. Export and finish — Take your Brand DNA document and go
```

### Request outputs directly:

```
Create a stakeholder presentation from my Brand DNA
```

```
Generate a one-page executive summary of my brand
```

```
Build a PDF brand book with all my brand guidelines
```

```
Write social media bios for my brand across all platforms
```

---

## Output Details

### Brand DNA Document (Primary Output)

A structured markdown document with 11 components:

- **Purpose** — Why the brand exists beyond profit
- **Vision** — The future state the brand is working toward
- **Mission** — What the brand does, for whom, and how
- **Core Values** — 3-5 non-negotiable principles
- **Brand Personality** — Archetype and human traits
- **Brand Voice & Tone** — How the brand communicates
- **Positioning** — Target audience, category, differentiation, positioning statement
- **Brand Story** — Narrative arc from origin to vision
- **Visual Identity Direction** — Strategic creative brief
- **Tagline / Mantra** — 3-5 options
- **Brand Do's and Don'ts** — Behavioral guidelines

### Stakeholder Presentation

12-slide PPTX with speaker notes:

| Slide | Content |
|-------|---------|
| 1 | Title (brand name + tagline) |
| 2 | The Problem (audience pain points) |
| 3 | Purpose (why we exist) |
| 4 | Vision & Mission |
| 5 | Core Values |
| 6 | Personality |
| 7 | Voice |
| 8 | Positioning |
| 9 | Story |
| 10 | Visual Direction |
| 11 | Do's & Don'ts |
| 12 | Summary + CTA |

### One-Page Executive Summary

Condensed Brand DNA:
- Essence (purpose/vision/mission in 3 sentences)
- Identity (values, personality, voice in bullets)
- Position (positioning statement)
- Tagline

### Social Media Bios

Platform-optimized copy:
- Twitter/X (160 chars)
- LinkedIn (2000 chars)
- Instagram (150 chars)
- TikTok (80 chars)

---

## Project Structure

```
Brand_Skills/
├── .claude-plugin/
│   └── marketplace.json              # Plugin manifest
├── CLAUDE.md                         # Claude Code guidance
├── README.md                         # This file
└── skills/
    └── brand-dna/
        ├── SKILL.md                  # Main skill definition (5 modes)
        └── references/
            ├── framework-components.md   # 11 component definitions
            ├── workshop-questions.md     # Workshop question bank
            ├── presentation-template.md  # Slide structure
            ├── audit-rubric.md           # Scoring criteria
            └── voice-contexts.md         # Voice sample contexts
```

---

## Examples

### Example 1: Full Workshop Flow

```
User: Help me figure out my brand for a productivity app for ADHD adults

Claude: [Asks Purpose & Origin questions]

User: [Answers about personal experience with ADHD, frustration with existing tools]

Claude: [Synthesizes into Purpose and Vision, moves to Audience & Problem]

... [continues through all 9 sections] ...

Claude: Here's your complete Brand DNA for [App Name]!

Your Brand DNA is complete! What would you like to create next?
1. Stakeholder presentation...
```

### Example 2: Quick Audit

```
User: Audit my brand. Here's our website: example.com and our brand guidelines PDF.

Claude: [Reviews materials, scores each component]

Brand Health Score: 38/62.5 (Developing)

Strengths:
- Voice & Tone (4/5): Clear, consistent, well-documented
- Visual Direction (4/5): Distinctive and well-executed

Critical Gaps:
- Purpose (2/5): Too generic, could apply to any competitor
- Values (2/5): Standard corporate values without teeth

Recommended: Run mini-workshops for Purpose and Values sections.
Would you like to do that now?
```

### Example 3: Direct Creation with Outputs

```
User: Here's everything about my brand [provides details]. Structure it and then create a presentation.

Claude: [Maps to framework, identifies gaps, generates Brand DNA]

Here's your Brand DNA. I noticed gaps in Brand Story and Visual Direction — want to fill those in?

User: Skip for now, just make the presentation.

Claude: [Generates 12-slide PPTX with speaker notes]
```

---

## Version History

- **v2.0.0** — Added brand audit, voice samples, competitive positioning, post-workshop menu, presentation output, executive summary, PDF brand book, social media bios
- **v1.0.0** — Initial release with guided workshop and direct creation modes

## License

Apache 2.0
