# rulesets

Curated rules for AI coding assistants to generate consistent, idiomatic code.

## Rulesets

RUST_RULES.md contains conventions for Rust workspaces, dependency organization, documentation, and binary crate placement.

## Usage

Claude Code loads all .md files from .claude/rules/ automatically.

```bash
cp RUST_RULES.md /path/to/project/.claude/rules/rust.md
```

Cursor uses .cursor/rules/ with .mdc extension. YAML frontmatter can scope rules to file patterns.

```bash
cp RUST_RULES.md /path/to/project/.cursor/rules/rust.mdc
```

## Ruleset Style

Keep rules technical and plaintext. Avoid bullet points. Use short declarative sentences that state conventions directly.

## License

MIT License - see LICENSE.
