# Ruby Skills

Ruby's ecosystem has many version managers, a rapidly evolving typing and tooling landscape, and documentation scattered across multiple sources.

This Claude Code plugin helps Claude navigate each of these — activating the correct Ruby environment and pointing to authoritative docs.

## Installation

**From terminal:**

```bash
claude plugin marketplace add st0012/ruby-skills
claude plugin install ruby-skills@ruby-skills
```

**From a Claude session:**

```bash
/plugin marketplace add st0012/ruby-skills
/plugin install ruby-skills@ruby-skills
```

## What to Expect

After installation, start a Claude Code session in any Ruby project — no configuration needed. The plugin activates automatically.

- Detects your version manager and project Ruby version, then activates it for all commands
- Supports chruby, rbenv, rvm, asdf, mise, rv, and shadowenv
- Provides Claude with a curated map of authoritative documentation sources, including version-specific docs and the references about the Ruby typing ecosystem

See the [technical reference](plugins/ruby-skills/skills/ruby-version-manager/README.md) for detection internals.

## Acknowledgements

The version manager detection logic is based on [Ruby LSP's VS Code extension](https://github.com/Shopify/ruby-lsp/tree/main/vscode) by Shopify.

## Contributing

Feedback, use cases, issue reports, and contributions are all welcome on [GitHub](https://github.com/st0012/ruby-skills).

## License

MIT License - see [LICENSE](LICENSE) for details.
