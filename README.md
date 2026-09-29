# Scaling Silicon Valley Style

The playbook from Roland Siebelink's *Scaling Silicon Valley Style*, as AI
skills you run in Claude, for founders past product-market fit.

## Install

```bash
npx skills add midstage/ssvs
```

Or with pnpm: `pnpm dlx skills add midstage/ssvs`. Or copy
`skills/ssvs-start-here/` into your own `.claude/skills/` directory.

Then ask Claude: **"What stage is my startup in?"**

## What's free vs. connected

**Free, in this repo:** `ssvs-start-here` places your company on the book's
six-stage Scaleup Roadmap (Applicant, Freshman, Sophomore, Junior, Senior,
Graduate) in three questions and names the competence to master next.

**Connected (paid subscription):** the full SSVS kit, served live from
Midstage so it stays current:

| Skill | For when |
|---|---|
| `ssvs-stage-diagnosis` | You want all seven roadmap dimensions scored and your blind spots named |
| `ssvs-painkiller-pmf-test` | You're not sure you really have product-market fit |
| `ssvs-series-readiness` | You're about to raise a Series A, B or C |
| `ssvs-core-decisions` | You hired more people and got slower |
| `ssvs-channel-economics` | You're not sure your sales channel fits your customer value |
| `ssvs-accountability-chart` | Nobody quite owns anything |
| `ssvs-quarterly-rocks` | Your planning offsites don't change anything |
| `ssvs-sandbox-focus` | You're spread across too many products, segments and markets |
| `ssvs-beachhead-whole-product` | You need to win mainstream buyers, not early adopters |
| `ssvs-leverage-decisions` | The founders are the bottleneck on every decision |

`ssvs-start-here` walks you through connecting. USD 19 a month, cancel
any time.

## Reference

| Guide | What it covers |
|---|---|
| [`01-scaleup-roadmap.md`](reference/01-scaleup-roadmap.md) | The six stages and seven dimensions, and how to read them |
| [`02-about-the-book.md`](reference/02-about-the-book.md) | The book's premise and what Volume 1 covers |
| [`03-connecting-and-billing.md`](reference/03-connecting-and-billing.md) | What connecting needs, what we store, how to cancel |

## Repo layout

```
ssvs/
├── README.md
├── skills/
│   └── ssvs-start-here/SKILL.md    free stage placement + connect steps
└── reference/
    ├── 01-scaleup-roadmap.md
    ├── 02-about-the-book.md
    └── 03-connecting-and-billing.md
```

## FAQ

**Does it work in ChatGPT, Claude Desktop or claude.ai?**
The free skill works anywhere you can paste a `SKILL.md`. The connected kit works in Claude (web, desktop app or Claude Code) and ChatGPT (Plus or higher): add `https://skills.midstage.ac/mcp` as a custom connector.

**Why aren't the paid skills in this repo?**
They're served live from Midstage, so every subscriber always runs the current version.

**Is my conversation sent to Midstage?**
No. See [`03-connecting-and-billing.md`](reference/03-connecting-and-billing.md) for exactly what is.
