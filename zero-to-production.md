Toolchain 
=========

Check versions
--------------

rustc --version
cargo --version

Watch for code changes
----------------------

cargo install cargo-watch

cargo watch -x check
cargo watch -x check -x test -x run

CI Steps
--------

Tests:

cargo test

Code coverage:

cargo install cargo-tarpaulin
cargo tarpaulin --ignore-tests

Linting:

rustup component add clippy
cargo clippy

In CI pipeline: cargo clippy -- -D warnings
Mute a warning: #[allow(clippy::lint_name)] 
Mute a warning at project level:
- via clippy.toml
- via project-level directive: #![allow(clippy::lint_name)]

Formatting:

rustup component add rustfmt
cargo fmt

In CI pipeline: cargo fmt -- --check

Security vulnerabilities:

cargo install cargo-audit
cargo audit







