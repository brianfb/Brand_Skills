# Brand Skills

A Claude Code plugin for strategic brand building. Includes the **Brand DNA Framework** skill — a structured approach to defining, discovering, and documenting brand identity.

## Skills

### Brand DNA (`brand-dna`)

Build a complete Brand DNA framework from scratch. Supports two modes:

**Guided Workshop Mode** — Step-by-step brand discovery through strategic questioning. Walks you through 9 sections:

1. Purpose & Origin
2. Audience & Problem
3. Differentiation & Positioning
4. Values & Beliefs
5. Personality & Character
6. Voice & Communication
7. Brand Story
8. Visual & Sensory Direction
9. Tagline & Synthesis

**Direct Creation Mode** — Provide your existing brand information and get it structured into a complete Brand DNA document with gap analysis.

### Output

A structured markdown document covering:

- Purpose, Vision, and Mission
- Core Values
- Brand Personality (archetype + traits)
- Brand Voice & Tone (with contextual tone mapping and examples)
- Positioning (audience, category, differentiation, positioning statement)
- Brand Story (narrative arc)
- Visual Identity Direction
- Tagline options
- Brand Do's and Don'ts

## Installation

Install directly in Claude Code:

```
/install-plugin /path/to/Brand_Skills
```

Or install from GitHub:

```
/install-plugin https://github.com/brianbuschmann/Brand_Skills
```

## Project Structure

```
Brand_Skills/
├── .claude-plugin/
│   └── plugin.json                       # Plugin manifest
└── skills/
    └── brand-dna/
        ├── SKILL.md                      # Main skill definition
        └── references/
            ├── framework-components.md   # Detailed component definitions & examples
            └── workshop-questions.md     # Full workshop question bank
```

## License

Apache 2.0
