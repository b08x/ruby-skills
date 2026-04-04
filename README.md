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

### `ruby-version-manager`

Detects your version manager and project Ruby version, then activates it for every shell command. Supports chruby, rbenv, rvm, asdf, mise, rv, and shadowenv.

- Reads `.ruby-version`, `.tool-versions`, `.mise.toml`, or `Gemfile` to determine the required version
- Handles multi-manager environments — prompts you to set a preference if more than one is detected
- Offers to install missing Ruby versions
- Works around Claude Code's non-persistent shell by chaining activation with every command

See the [technical reference](plugins/ruby-skills/skills/ruby-version-manager/README.md) for detection internals.

### `ruby-resource-map`

Points Claude to authoritative documentation sources so it doesn't hallucinate APIs or rely on outdated references.

- Version-specific docs for Ruby 3.2–4.0 and master
- Core vs bundled vs default gem distinctions
- Ruby typing ecosystem: Sorbet (RBI) and RBS, including Tapioca, Spoom, Steep, and RBS inline comments
- Blocks known-bad sources (ruby-doc.org, apidock.com)

## Acknowledgements

The version manager detection logic is based on [Ruby LSP's VS Code extension](https://github.com/Shopify/ruby-lsp/tree/main/vscode) by Shopify.

## Contributing

Feedback, use cases, issue reports, and contributions are all welcome on [GitHub](https://github.com/st0012/ruby-skills).

## License

MIT License - see [LICENSE](LICENSE) for details.
