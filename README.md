# Portee Skill for Antigravity & Codex

**Portee** is an advanced AI coding skill adapted from ClaudeKit's *Xia*. It provides a structured, 6-phase workflow for extracting, comparing, and porting features from external repositories into your local project with idiomatic accuracy.

## Features

- **6-Phase Pipeline**: Recon, Map, Analyze, Challenge, Plan, Deliver.
- **Idiomatic Porting**: Rewrites external code to match your local project's style and patterns.
- **Comparison Mode**: Generates deep analysis reports comparing implementations without modifying code.
- **Subagent-Aware**: Efficiently uses browser and research tools to "pack" source repositories when external tools are missing.

## Installation

To install this skill into your Antigravity or Gemini CLI environment:

1. Clone this repository into your `skills` directory:
   ```bash
   cd ~/.gemini/antigravity/skills
   git clone https://github.com/kentng84/Portee.git portee
   ```

2. Register the skill in your `.antigravity-install-manifest.json` by adding `"portee"` to the `entries` list.

3. Restart your AI assistant.

## Usage

| Command | Action |
|---------|--------|
| `portee <source> [feature] --port` | Default. Port a feature idiomatically. |
| `portee <source> [feature] --compare` | Analysis report only. |
| `portee <source> [feature] --improve` | Port and refactor. |

## Credits

Based on the **Xia** skill from [ClaudeKit](https://docs.claudekit.cc/).
