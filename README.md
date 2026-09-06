# BotOps

The BotOps lifecycle skill for Matthew’s Grok Bot fleet, shaped to the [Agent Skills](https://agentskills.io/specification) standard.

It is the single lifecycle for that fleet: Chief of Staff (L1) → domain owners (L2) → one-shot temps and cadence runners (L3), with Notion as the source of record. Load this skill for non-trivial fleet work rather than splitting the lifecycle across other skills.

## Skill layout

```
botops/
└── SKILL.md
```

The skill directory is `botops/`. Its folder name must match frontmatter `name: botops`.

## Install / usage

Clone this repository and load the `botops/` skill directory in any Agent Skills–compatible client. Copy or symlink that folder into the client’s skills path (project-level `.agents/skills/botops`, or a user-level directory such as `~/.agents/skills/botops` or `~/.cursor/skills/botops`).

```bash
git clone https://github.com/granda/botops.git
cp -R botops ~/.agents/skills/botops
```

Compatible clients discover `SKILL.md` and activate the skill from its `name` and `description`.

## How I Run Grok Bot

Narrative context for this skill lives in the post **How I Run Grok Bot** (slug: `how-i-run-grok-bot`).

- Canonical public URL: https://granda.org/en/2026/09/06/how-i-run-grok-bot/

The post is **not live on production yet** (that URL currently redirects to `/en/`). Until publish, also use:

- Draft PR: https://github.com/granda/blog/pull/187
- Preview: https://146da0e9.granda.pages.dev/en/2026/09/06/how-i-run-grok-bot/

Update this README to the live canonical URL only once the post is published (update on publish).

## Validate

```bash
npx skills-ref validate ./botops
```

## License

MIT. See [LICENSE](LICENSE).
