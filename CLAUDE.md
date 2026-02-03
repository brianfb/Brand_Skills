# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Brand Skills is a Claude Code plugin for strategic brand building. It provides the **Brand DNA Framework** skill — a content-driven plugin (no build system, no dependencies, no compiled code) that helps users define, discover, document, and audit brand identities through structured questioning, multiple output formats, and cross-skill integrations.

## Architecture

This is a pure content plugin — all functionality is defined through markdown and JSON, with no code compilation or runtime dependencies.

```
.claude-plugin/marketplace.json   ← Plugin manifest (entry point for Claude Code)
skills/brand-dna/
  SKILL.md                        ← Skill definition: 5 modes, output formats, quality standards
  references/
    framework-components.md       ← 11 component definitions with weak/strong examples
    workshop-questions.md         ← 9-section question bank (90+ questions)
    presentation-template.md      ← 12-slide structure for stakeholder presentations
    audit-rubric.md               ← Scoring criteria for brand health assessment
    voice-contexts.md             ← 10 contexts for voice sample generation
```

**marketplace.json** registers the plugin with Claude Code. **SKILL.md** is the execution guide that defines five operating modes and multiple output formats. The reference files provide the knowledge base that SKILL.md points to.

## Key Concepts

### Modes

1. **Guided Workshop Mode**: Step-by-step brand discovery through 9 sequential sections, presenting 2-4 questions per turn
2. **Direct Creation Mode**: User provides existing brand info, which gets mapped to the 11 framework components with gap analysis
3. **Brand Audit Mode**: Evaluate existing brand materials against the framework with 1-5 scoring and gap analysis
4. **Voice Sample Generator**: Generate 10 voice samples across different contexts (headlines, errors, social, support, etc.)
5. **Competitive Positioning Helper**: Deep-dive competitive analysis with white space identification and positioning options

### Output Formats

- **Brand DNA Document**: Primary markdown output with all 11 framework components
- **Stakeholder Presentation (PPTX)**: 10-12 slide deck via `document-skills:pptx`
- **One-Page Executive Summary**: Condensed Brand DNA for quick reference
- **PDF Brand Book**: Comprehensive document via `document-skills:pdf`
- **Social Media Bios**: Platform-specific copy for Twitter, LinkedIn, Instagram, TikTok
- **Voice Samples**: Brand voice demonstrated across 10 contexts
- **Audit Report**: Scored assessment with recommendations

### Post-Workshop Menu

After completing a Brand DNA, users are presented with a menu to generate additional outputs (presentation, summary, brand book, social bios, voice samples) or export and finish.

### Cross-Skill Integration

This skill invokes other document skills for output generation:
- `document-skills:pptx` for stakeholder presentations
- `document-skills:pdf` for comprehensive brand books

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

## Version History

- **v2.0.0**: Added brand audit mode, voice sample generator, competitive positioning helper, post-workshop menu, presentation output, executive summary, PDF brand book, and social media bios
- **v1.0.0**: Initial release with guided workshop and direct creation modes

## License

Apache 2.0
