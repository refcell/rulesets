RUST RULES

Modules should have doc strings at the top of the file using //! syntax.

lib.rs files should include crate-level attributes in this order:
#![doc = include_str!("../README.md")]
#![doc(issue_tracker_base_url = "...")]
#![cfg_attr(docsrs, feature(doc_cfg, doc_auto_cfg))]
#![warn(missing_docs)]
#![forbid(unsafe_code)]

Lints are defined in the workspace Cargo.toml under [workspace.lints.*] sections.
Crates inherit lints by adding [lints] workspace = true to their Cargo.toml.

Dependencies should not specify versions in crate Cargo.toml files.
Use workspace = true to inherit from the workspace.
Optional dependencies use { workspace = true, optional = true }.

Group workspace dependencies into logical sections with comments:
# Internal crates
# DataFrames
# Async runtime
# Serialization
# HTTP client
# Error handling

Within each group order dependencies by line length (shortest to longest).
This creates a waterfall visual effect and makes scanning easier.

Crates inherit package metadata from workspace.package using .workspace = true:
version.workspace = true
edition.workspace = true
rust-version.workspace = true
license.workspace = true
repository.workspace = true

Each crate should have a README.md file in its root directory.
This enables the #![doc = include_str!("../README.md")] pattern for nice crate documentation.

Binary crates should be placed in the top-level bin/ directory.
Keep main.rs files minimal, ideally under 100 lines.
Binaries should parse arguments and delegate to library code.
