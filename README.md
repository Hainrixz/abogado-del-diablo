# 😈 Abogado del Diablo (Devil's Advocate)

> The skill that turns Claude against you and tears your idea apart.

**English · [Español](./README.es.md)**

A Claude Code skill (and plugin) that takes on the role of a hostile devil's
advocate: it grabs your idea, plan, pitch, or an entire project and critiques it
hard — no validation, no softening — until it hands you a blunt verdict with a
prioritized list of what to fix first.

Built by the [tododeia](https://www.tododeia.com) community.
Full guide (Spanish): **[tododeia.com/community/abogado-del-diablo](https://www.tododeia.com/community/abogado-del-diablo)**

---

## Why it exists

By default, Claude tends to agree with you. It validates, softens, and finds the
upside in everything. That feels good and ruins decisions. When you're about to
bet time, money, or your reputation, you don't need "wow, great idea" — you need
someone to find the cracks **before** the market does.

This skill is that someone. It assumes your idea will fail and sets out to prove
it — not out of cruelty, but because every crack it finds here is one you no longer
discover late and expensive.

## What it does

- **Bans flattery.** No compliments, no "it has potential, but…".
- **Attacks across eight angles:** false assumptions · market · competition ·
  viability · numbers · execution · pre-mortem (how it dies in 12 months) · blind spot.
- **Researches** real-world failures of similar ideas (when web tools are available).
- **Analyzes whole projects** in Claude Code (reads your files) and can fan out
  subagents in parallel, one per angle, for a deep demolition.
- **Ends constructive:** blunt verdict → cracks by severity → the one that kills it
  → what to fix first. Brutal to the idea, never to you.

## Install

### Option A — Claude Code plugin (recommended)

Inside a Claude Code session:

```
/plugin marketplace add Hainrixz/abogado-del-diablo
/plugin install abogado-del-diablo@abogado-del-diablo
```

Then invoke it with `/abogado-del-diablo`.

### Option B — Manual skill

Copy `skills/abogado-del-diablo/` into `~/.claude/skills/` (or `.claude/skills/`
inside your project). Or download [`SKILL.md`](./SKILL.md) and drop it at
`~/.claude/skills/abogado-del-diablo/SKILL.md`.

### Option C — No install (chat / Cowork)

Paste the contents of [`SKILL.md`](./SKILL.md) as the first message in claude.ai or
Cowork, then your idea below it. Same devil's advocate, nothing to install.

## Usage

```
/abogado-del-diablo

I want to launch a healthy-snack subscription box at $25/month.
```

Other forms:

- **Whole project:** `/abogado-del-diablo --proyecto`
- **Deep demolition (subagents):** `/abogado-del-diablo --demolicion`
- **Natural language:** "tear this idea apart, no filter", "tell me why it'll fail",
  "red team this".

> The skill responds in the user's language (Spanish by default, since it's built
> for a Spanish-first community).

## What you get

```
VERDICT
This isn't a startup, it's a grocery-margin business dressed up as tech, and the
numbers don't add up from day one. Four cracks, deadliest first:

1. The economics don't close — that's problem number one.
   - The hit: ...
   - Why it's lethal: ...
   - What would have to be true: ...
...

THE ONE THAT KILLS IT
Unit economics.

IF YOU INSIST, FIX THIS FIRST
1. ...
```

Full example in [`skills/abogado-del-diablo/references/ejemplos.md`](./skills/abogado-del-diablo/references/ejemplos.md).

## Structure

```
abogado-del-diablo/
├── .claude-plugin/{marketplace.json, plugin.json}
├── commands/abogado-del-diablo.md          # the slash command
├── skills/abogado-del-diablo/
│   ├── SKILL.md                            # the skill's brain
│   └── references/{angulos.md, ejemplos.md}
└── SKILL.md                                # copy for download / direct paste
```

## License

MIT. Use it, modify it, share it.

---

Built by [tododeia](https://www.tododeia.com) and maintained by
[@Hainrixz](https://github.com/Hainrixz). Not affiliated with Anthropic. If it
saved you from a bad decision, drop a ⭐ and pass it to someone who needs the truth.
