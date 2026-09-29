# Publish checklist (do not submit without Raz yes)

1. Repo: https://github.com/ramihaly/creativelisting-plugin (public)
2. Preferred submit: https://cursor.directory/plugins/new — sign in with GitHub, paste the repo URL
3. Alternate: https://cursor.com/marketplace/publish
4. Confirm marketplace listing name `creative-listing` is unique
5. Logo: `assets/logo.png` (512×512) is in the repo; Agent Plugins `plugin.json` has no `logo` field (closed schema). If the form asks for a logo, upload `assets/logo.png`.
6. Local package: root `plugin.json` + `mcp.json` (Agent Plugins 1.0.0), skill frontmatter, README, LICENSE, no API keys, prod MCP URL only
7. OAuth: URL-only `mcp.json` — OAuth 2.1 + PKCE / DCR. Do not use legacy API keys.
8. **Do not** submit until Raz explicitly says yes.

## Package layout

```
plugin.json
mcp.json
skills/creative-listing-getting-started/SKILL.md
assets/logo.png
README.md
LICENSE
PUBLISH.md
```
