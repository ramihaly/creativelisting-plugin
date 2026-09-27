# Creative Listing — Cursor / Agent Plugin

Search, create, and manage creative real-estate deals on [Creative Listing](https://www.creativelisting.com) (seller-financed, subject-to, rentals) from Cursor and other Agent Plugins clients.

![Creative Listing](assets/logo.png)

## Install

1. Install from the Cursor marketplace once published, **or** load this repo as a local plugin.
2. Complete OAuth when Cursor prompts you for `creativelisting.com`.
3. Sign in with a free [Creative Listing](https://www.creativelisting.com) account.

Publish form (maintainers): https://cursor.com/marketplace/publish

## MCP

Remote Streamable HTTP MCP (URL only — no API key in the plugin):

```json
{
  "mcpServers": {
    "creative-listing": {
      "type": "streamable-http",
      "url": "https://www.creativelisting.com/api/mcp"
    }
  }
}
```

Auth is **OAuth 2.1 + PKCE** with open Dynamic Client Registration. The client discovers:

- Authorization server: `https://www.creativelisting.com/.well-known/oauth-authorization-server`
- Protected resource: `https://www.creativelisting.com/.well-known/oauth-protected-resource`

Scopes: `mcp:read`, `mcp:write` (writes require `mcp:write` at consent).

Do **not** use legacy Creative Listing API keys for MCP (HTTP 410). Do **not** point installs at a stage host.

## Tools

| Tool | Purpose |
| --- | --- |
| `search` | Search public listings |
| `fetch` | Fetch one listing by id |
| `get_my_matches` | Listings matching buyer preferences |
| `get_my_preferences` | Read buyer preferences |
| `get_my_listings` | Your listings |
| `create_listing` | Create a listing (`mcp:write`) |
| `update_listing` | Update a listing (`mcp:write`) |
| `manage_listing_photos` | Manage listing photos (`mcp:write`) |

## Example prompts

- Find seller-financed single-family listings under $300k in Arizona.
- Show the deals that match my buyer preferences.
- Create a new listing for my property at \<address\> and add these photos.
- Update the price on my \<address\> listing to $X.

## Docs & legal

- Help: https://www.creativelisting.com/help
- Privacy: https://www.creativelisting.com/api/legal/privacy
- Terms: https://www.creativelisting.com/terms
- Support: info@creativelisting.com

## License

MIT — see [LICENSE](LICENSE).
