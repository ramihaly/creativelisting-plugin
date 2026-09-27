---
name: creative-listing-getting-started
description: Use when the user wants to find, create, or manage Creative Listing real-estate deals from chat (seller-financed, subject-to, rentals). Covers first-run OAuth connect and the eight listing tools.
---

# Creative Listing — getting started

## When to use

- Search creative real-estate deals (seller-financed, subject-to, rentals)
- Show matches against the signed-in user’s buyer preferences
- Create or update the user’s own listings, including photos

## Setup

1. Install this plugin from the Cursor marketplace (or load the local package).
2. When prompted, complete OAuth for `creativelisting.com` (OAuth 2.1 + PKCE; open Dynamic Client Registration). A free Creative Listing account is required.
3. Prefer the **prod** MCP only: `https://www.creativelisting.com/api/mcp`. Never point a public install at a stage host.
4. Do **not** use legacy Creative Listing API keys for MCP — the server rejects them (HTTP 410). Auth is OAuth only.

## Tools (8)

| Tool | Purpose |
| --- | --- |
| `search` | Search public listings |
| `fetch` | Fetch one listing by id |
| `get_my_matches` | Listings matching the user’s buyer preferences |
| `get_my_preferences` | Read the user’s buyer preferences |
| `get_my_listings` | Listings owned by the signed-in user |
| `create_listing` | Create a listing (needs `mcp:write`) |
| `update_listing` | Update a listing (needs `mcp:write`) |
| `manage_listing_photos` | Add/remove listing photos (needs `mcp:write`) |

Write tools require the `mcp:write` scope at consent.

## Example prompts

- Find seller-financed single-family listings under $300k in Arizona.
- Show the deals that match my buyer preferences.
- Create a new listing for my property at \<address\> and add these photos.
- Update the price on my \<address\> listing to $X.

## Safety

- Writes need `mcp:write` and apply only to the authenticated user’s own account.
- Never request or paste legacy Creative Listing API keys for MCP.
- Never use stale `*_deal` tool names.
