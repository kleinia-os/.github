# Contributing to Kleinia

Thanks for your interest in Kleinia! Bug reports, docs fixes, translations,
testing on real hardware and code are all welcome contributions.

> Individual repositories may add their own `CONTRIBUTING.md` with build
> instructions. Where they differ from this page, the repository's file wins.

## Ways to help

- **Try it and report what breaks.** Kleinia 0.1 Aloe, the first technical
  preview, is almost there ([kleinia.io/download](https://kleinia.io/download)).
  Once it's out, hardware reports (laptops, GPUs, Wi-Fi) are especially valuable.
- **Improve the docs.** Every page on [docs.kleinia.io](https://docs.kleinia.io)
  has an "Edit page" link that goes to [`kleinia-web`](https://github.com/kleinia-os/kleinia-web).
- **Translate.** The website and docs ship in English and Simplified Chinese;
  more languages are welcome. Say hello on [Discord](https://kleinia.io/discord) or open an issue first so we can set up the locale.
- **Write code.** Look for issues labelled `good first issue` or `help wanted`.

## Where things live

| Area | Repository |
|---|---|
| Image recipe, system files, CI | `kleinia` |
| Agent runtime and CLI (`agentd`, `agentctl`, system agents) | `kleinia-agents` |
| Model gateway | `llmgw` |
| Context and memory | `ctxd` |
| Tracing and token accounting | `agenttrace` |
| Kernel patches | `kleinia-kernel` |
| Installer | `installer` |
| Brand assets (logo, palette, fonts, wallpapers) | `branding` |
| Website and docs | `kleinia-web` |

Not sure? Open the issue in [`kleinia`](https://github.com/kleinia-os/kleinia)
and we'll move it.

## Before you start on something big

Open an issue (or start a thread in `#feedback` on [Discord](https://kleinia.io/discord)) **before** writing a large change, a new
component or anything that touches a public interface (D-Bus APIs, the
`agent://` scheme, CLI flags, config formats). A short design note saves both
of us a rewrite.

## Pull requests

1. Fork the repository and branch from its default branch.
2. Keep each PR to one logical change; split refactors from behaviour changes.
3. Add or update tests where the repository has them, and make sure they pass.
4. Update the docs if you change user-visible behaviour.
5. Fill in the PR template, and link the issue it fixes (`Fixes #123`).

A maintainer will review your PR; expect questions, as that's normal. We merge
with squash or rebase to keep history linear.

### Commit messages

We use [Conventional Commits](https://www.conventionalcommits.org/) style:

```
fix(llmgw): retry upstream on 429 with backoff

Longer explanation of what and why, wrapped at ~72 columns.
```

Common types: `feat`, `fix`, `docs`, `refactor`, `test`, `ci`, `chore`.

### Sign your work (DCO)

Every commit must carry a `Signed-off-by` line certifying the
[Developer Certificate of Origin](https://developercertificate.org/):

```bash
git commit -s
```

Kernel patches additionally follow the upstream Linux
[submitting patches](https://docs.kernel.org/process/submitting-patches.html) rules.

## Licensing

By contributing, you agree that your contribution is licensed under the
license of the repository you're contributing to (see its `LICENSE` file).

## AI-assisted contributions

Kleinia is a system for agents, so using AI tools to help you write code or
docs is fine. You are still the author: review and test everything you submit,
make sure you have the right to contribute it, and be ready to explain it in
review. Don't submit unreviewed, bulk-generated PRs or issues.

## Code of Conduct

Everyone taking part is expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
