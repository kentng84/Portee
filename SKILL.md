---
name: portee
description: Extract, compare, port, or adapt features from external repositories into your current project (Antigravity/Codex).
risk: medium
source: community
---

# Portee (Xia adaptation)

Extract, compare, port, or adapt a feature from a GitHub repository or local repo into your current project. Study how another codebase implements something, then bring that implementation home — rewritten idiomatically for your local stack.

## 6-Phase Workflow

### 1. Recon
- **Pack Source**: Attempt `npx repomix` on the source. If unavailable, use `browser_subagent` (for GitHub) or recursive `list_dir`/`grep_search` to read files.
- **Scout Local**: Analyze your current project structure to find integration points.
- **Context**: Use `search_web` to understand the library's design philosophy and trade-offs.

### 2. Map
- **Inventory**: Identify core logic, state management, APIs, configs, types, and tests in the source.
- **Dependencies**: Cross-reference source requirements with your local environment (`package.json`, `requirements.txt`, etc.).

### 3. Analyze
- **The "Why"**: Trace execution paths. Understand *why* decisions were made, not just *how* the code looks.
- **Contract Discovery**: Identify implicit assumptions or hidden side effects in the source.

### 4. Challenge
- **Anti-Assumption**: Generate 5+ challenge questions about the port (e.g., "Will this bridge correctly with our existing state management?").
- **Decision Matrix**: Evaluate risks if source assumptions don't match local reality.

### 5. Plan
- **Implementation Design**: Create a detailed plan (using the `writing-plans` skill) including a rollback strategy.
- **Comparison Report**: If in `--compare` mode, produce a side-by-side analysis instead of code changes.

### 6. Deliver
- **Execution**: Implement the plan (using execution-focused skills or native tools).
- **Final Polish**: Ensure code matches your local coding standards and project idioms.

## Usage Guide

| Command | Action |
|---------|--------|
| `portee <source> [feature] --port` | Default. Idiomatic rewrite for your stack. |
| `portee <source> [feature] --compare` | Analysis report only. No changes. |
| `portee <source> [feature] --improve` | Refactor and enhance while porting. |
| `portee <source> [feature] --auto` | Auto-approve approval gates. |

## Examples

- `portee react-query "infinite scroll" --port`
- `portee owner/repo "auth middleware" --improve`
- `portee ./local/path "state management" --compare`

## Related Skills
- [writing-plans](file:///C:/Users/ngtha/.gemini/antigravity/skills/writing-plans/SKILL.md)
- [unit-testing-test-generate](file:///C:/Users/ngtha/.gemini/antigravity/skills/unit-testing-test-generate/SKILL.md)
- [analyze-project](file:///C:/Users/ngtha/.gemini/antigravity/skills/analyze-project/SKILL.md)
