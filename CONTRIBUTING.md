# Contributing to Atlas

Thanks for helping improve Atlas — the authentication & user-management platform.

## How this org is organized

Most repositories here are the **public home of a published package** (npm
`@atlasauth/*`, crates.io `atlasauth`, Maven Central `net.atlasauth:*`, pub.dev
`atlas_auth`, PyPI, RubyGems, Packagist, the Terraform & Pulumi providers) or a
**runnable quickstart/demo**. Each repo's README has its install + usage.

## Reporting bugs

Open an issue on the relevant repo using the **Bug report** template. Include the
SDK/package version, runtime (Node/JVM/Swift/etc.), a minimal repro, and what you
expected vs. saw. For anything involving keys, tokens, or account data, redact
secrets — and if it's a vulnerability, **do not** open a public issue: follow
[SECURITY.md](./SECURITY.md).

## Proposing changes

- Open an issue first for anything non-trivial so we can agree on the approach.
- Keep PRs focused; match the surrounding code's style; add/adjust tests.
- The SDKs mirror one code-derived API contract, so a change that alters behavior
  usually belongs in the platform, not a single SDK — flag it in the issue.

## Questions & support

- **Docs:** https://atlasauth.net/docs
- **API reference:** https://api.atlasauth.net/v1/openapi.json
- Product questions that aren't bugs: use the repo's Discussions or the support
  links in the issue chooser.
