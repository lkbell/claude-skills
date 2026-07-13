# agent-skills — personal skills marketplace

A GitHub repo that acts as a Claude plugin marketplace. Add it once per surface
(Web chat, Desktop chat, Cowork) and its skills become available on all of them.

## Layout
- `.claude-plugin/marketplace.json` — registers this repo as the marketplace (`landon-hub`)
- `plugins/personal/.claude-plugin/plugin.json` — the `personal` plugin
- `plugins/personal/skills/<name>/SKILL.md` — one folder per skill (browse `plugins/personal/skills/` for the current set)

## Use it
1. In your assistant's plugin settings (Claude: **Customize → Plugins → "+" → Add marketplace → Add from a repository**) → `https://github.com/lkbell/agent-skills` → install the **personal** plugin.
2. Type `/` in a chat or Cowork task; the plugin's skills appear.
3. After adding or editing a skill, **refresh/sync the marketplace on each surface** to activate it.

## Authoring
Skills are authored by the assistant via the GitHub MCP connector (or git). Each skill is a
folder under `plugins/personal/skills/` containing a `SKILL.md` with YAML frontmatter
(`name`, `description`); the `description` is the trigger, so write it precisely.
