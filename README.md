# rulesets

A collection of rulesets for agentic programming assistants.

## Overview

This repository contains curated rules for various programming languages that help AI coding assistants generate consistent, idiomatic code following best practices.

### Available Rulesets

- **RUST_RULES.md** - Conventions for structuring Rust workspaces, organizing dependencies, writing documentation, and placing binary crates.

## Usage

For Claude Code, copy the file to your project's `.claude/rules/` directory as a markdown file. Claude automatically loads all `.md` files from this directory.

```bash
cp RUST_RULES.md /path/to/your/project/.claude/rules/rust.md
```

For Cursor, copy the file to `.cursor/rules/` and rename it with the `.mdc` extension. You can add YAML frontmatter to scope the rules to specific file patterns.

```bash
cp RUST_RULES.md /path/to/your/project/.cursor/rules/rust.mdc
```

## License

MIT License - see [LICENSE](LICENSE).
