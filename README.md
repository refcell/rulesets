# rust-rules

A concise Rust ruleset for agentic programming assistants.

## Overview

RUST_RULES.md contains conventions for structuring Rust workspaces, organizing dependencies, writing documentation, and placing binary crates. These rules help AI coding assistants generate consistent, idiomatic Rust code that follows workspace best practices.

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
