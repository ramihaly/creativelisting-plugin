# Publish checklist (do not submit without Raz yes)

1. Repo: https://github.com/ramihaly/creative-listing-plugin (public)
2. Form: https://cursor.com/marketplace/publish — paste the repo URL while signed into Cursor
3. Confirm marketplace listing name `creative-listing` is unique
4. Logo: `assets/logo.png` (512×512) is in the repo; Agent Plugins `plugin.json` has no `logo` field (closed schema). If the form asks for a logo, upload `assets/logo.png` or switch to a Cursor Plugin wrapper later.
5. Local package validated: root `plugin.json` + `mcp.json` (Agent Plugins 1.0.0), skill frontmatter, README, LICENSE, no legacy API keys, prod MCP URL only
6. OAuth: URL-only `mcp.json` is correct — AS/PRM well-knowns return 200; unauthenticated MCP returns 401 + `WWW-Authenticate` with resource_metadata (DCR open). Existing user MCP `Creative Listing` already uses this URL.
7. **Do not** click submit on cursor.com/marketplace/publish until Raz explicitly says yes.

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
