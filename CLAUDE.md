# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Brand Skills is a Claude Code plugin for strategic brand building. It provides the **Brand DNA Framework** skill — a content-driven plugin (no build system, no dependencies, no compiled code) that helps users define, discover, and document brand identities through structured questioning and documentation.

## Architecture

This is a pure content plugin — all functionality is defined through markdown and JSON, with no code compilation or runtime dependencies.

```
.claude-plugin/marketplace.json   ← Plugin manifest (entry point for Claude Code)
skills/brand-dna/
  SKILL.md                        ← Skill definition: modes, output format, quality standards
  references/
    framework-components.md       ← 11 component definitions with weak/strong examples
    workshop-questions.md         ← 9-section question bank (90+ questions)
```

**marketplace.json** registers the plugin with Claude Code. **SKILL.md** is the execution guide that defines two operating modes (Guided Workshop and Direct Creation). The two reference files provide the knowledge base that SKILL.md points to.

## Key Concepts

- **Guided Workshop Mode**: Step-by-step brand discovery through 9 sequential sections, presenting 2-4 questions per turn
- **Direct Creation Mode**: User provides existing brand info, which gets mapped to the 11 framework components with gap analysis
- **Output**: Always a structured markdown document following the skeleton defined in SKILL.md (Purpose → Vision → Mission → Values → Personality → Voice → Positioning → Story → Visual Direction → Tagline → Do's/Don'ts)
- **`strict: false`** in the manifest means the skill has flexibility in how it operates

## Installation

```
/install-plugin /path/to/Brand_Skills
```

Or from GitHub:

```
/install-plugin https://github.com/brianbuschmann/Brand_Skills
```

## No Build/Test/Lint

There are no build commands, test suites, or linters. All content is markdown and JSON. Validation is manual — ensure markdown structure is correct and that marketplace.json is valid JSON.

## License

Apache 2.0
