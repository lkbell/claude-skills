# agent-skills — personal skills marketplace

A GitHub repo that acts as Landon’s cross-agent skills marketplace. It currently uses the compatible plugin-marketplace layout shown below; installed surfaces load the same agent-agnostic skill library.

## Layout
- `.claude-plugin/marketplace.json` — registers this repo as the marketplace (`landon-hub`)
- `plugins/personal/.claude-plugin/plugin.json` — the `personal` plugin
- `plugins/personal/skills/<name>/SKILL.md` — one folder per skill (browse `plugins/personal/skills/` for the current set)

## Use it
1. In your assistant's plugin settings (Claude: **Customize → Plugins → "+" → Add marketplace → Add from a repository**) → `https://github.com/lkbell/agent-skills` → install the **personal** plugin.
2. Type `/` in a chat or Cowork task; the plugin's skills appear.
3. After adding or editing a skill, **refresh/sync the marketplace on each surface** to activate it.

## Authoring
Skills are authored by the assistant via a GitHub connector or git. Each skill is a folder under `plugins/personal/skills/` containing a `SKILL.md` with YAML frontmatter (`name`, `description`); the description is the trigger, so write it precisely.

Every release must pass two design gates:

1. **Agent-agnostic:** write the core workflow to roles and capabilities, not a provider, model, product, or surface. Use capability tiers instead of model names. Isolate unavoidable platform-specific mechanics in a labeled adapter or conditional section. Audit the frontmatter, body, resources, scripts, assets, and UI metadata before release.
2. **Brain-conformant:** any skill that touches Brain 2.0 must treat the Brain Operating Manual as the architecture. Point to canonical Brain policy/data rather than copying it; obey its write lanes, rituals, checks, and landing rules; never introduce a parallel memory, policy, task, status, or control system.

A product name is acceptable only when the skill’s actual subject is that product or within a clearly labeled compatibility path. Record the neutrality/conformance verdict during review, then bump the plugin manifest version for every shipped skill change.
