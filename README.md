# Axle Keys — Skills

Free, open skills that teach your AI agent to design real, manufacturable things in
[Axle Keys](https://axlekeys.com).

Axle Keys is a parametric CAD platform. You describe a physical object; your agent writes
the model, Axle builds the geometry on its server, checks it, and hands back something with
named parameters you can actually adjust. These skills are the choreography — install one,
and your agent knows the whole workflow.

## What's here

| Skill | Tier | What it does |
|---|---|---|
| [`brief-to-model`](skills/brief-to-model/) | Free | Turn a plain-English description into a real parametric 3D CAD model — built, dimension-verified, and shown back as a picture you can spin. |

## Connect Axle Keys to your agent

Everything here runs against the hosted Axle Keys MCP endpoint:

```
https://api.axlekeys.com/mcp
```

**Claude Code**

```bash
claude mcp add --transport http axle-keys https://api.axlekeys.com/mcp
```

**claude.ai / ChatGPT** — add it as a custom connector by URL in your connector settings.

## Install a skill

Clone this repo, then copy the skill you want into your project's skills directory:

```bash
git clone https://github.com/AxleKeys/skills.git axle-skills
cp -r axle-skills/skills/brief-to-model .claude/skills/
```

The clone is named `axle-skills` on purpose — this repo's folder is also called `skills`,
so cloning it bare leaves you with `skills/skills/…` and a copy command that misses by one
level.

On **claude.ai**, add the skill's `SKILL.md` to your project's knowledge instead.

Then just describe what you want to make. The skill triggers on its own.

## Access

Axle Keys is currently **invitation-only**. Signing up needs a Keyholder code — request one
at [axlekeys.com](https://axlekeys.com).

Already have a code? [Connect your agent](https://axlekeys.com/connect) and you're a minute
away from your first model.

## Contributing

Issues and skill ideas are very welcome — open an issue.

Skill authorship stays in-house for now. A skill is a set of instructions that your agent
obeys, so accepting one from a stranger is closer to accepting an advertisement than a
patch, and we'd rather get the review process right before opening that door.

## Licence

MIT — see [LICENSE](LICENSE).
