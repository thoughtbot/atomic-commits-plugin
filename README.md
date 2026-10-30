# atomic-commits-plugin

Claude Code plugin that guides agents to work in small, atomic commits and keep pull requests around ~200 lines. Inspired from [this thoughtbot blog post](https://thoughtbot.com/blog/working-iteratively).

## What it does

- **Skill** (`skills/atomic-commits/SKILL.md`) — teaches agents to plan atomic steps before coding, commit after each step, and split large PRs at natural seams.
- **Hook** (`hooks/check-diff-size.sh`) — monitors diff size after Edit/Write operations and nudges when it's time to commit or open a PR.

## Atomic Commit Criteria

Every commit must:

1. **Pass CI** — tests, linter, build all green
2. **Be deployable** — application is in a valid state
3. **Introduce no dead code** — no unreachable code, unused imports, or half-wired features

## Installation

Install via the [thoughtbot marketplace](https://github.com/thoughtbot/skills):

```
/plugin marketplace add thoughtbot/skills
/plugin install atomic-commits@skills
```

Or add directly:

```
/plugin install thoughtbot/atomic-commits-plugin
```

## License

Copyright © 2026 thoughtbot. It is free
software, and may be redistributed under the terms specified in the
[LICENSE] file.

[LICENSE]: https://github.com/thoughtbot/atomic-commits-plugin/blob/main/LICENSE

<!-- START /templates/footer.md -->
## About thoughtbot

![thoughtbot](https://thoughtbot.com/thoughtbot-logo-for-readmes.svg)

This repo is maintained and funded by thoughtbot, inc.
The names and logos for thoughtbot are trademarks of thoughtbot, inc.

We love open source software!
See [our other projects][community].
We are [available for hire][hire].

[community]: https://thoughtbot.com/community?utm_source=github
[hire]: https://thoughtbot.com/hire-us?utm_source=github

<!-- END /templates/footer.md -->
