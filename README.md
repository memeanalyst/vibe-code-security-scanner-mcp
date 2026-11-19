# Vibe Code Security Scanner — MCP Server

Scan any app built with AI (Codex, Cursor, Claude Code, Lovable, Bolt, v0, Replit) by URL for leaked OpenAI, Claude, Gemini and 60+ other API keys, open Supabase tables, source maps and missing security headers — and get an A–F security grade with fix prompts for every finding, as clean structured records from your AI agent or MCP client.

This repo is the MCP listing for the [Vibe Code Security Scanner](https://apify.com/magnova/vibe-code-security-scanner) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--vibe-code-security-scanner** — Scan an AI-built app by URL for leaked API keys, open databases, source maps and missing security headers. Returns structured records: findings by severity, an A–F grade, and fix prompts.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/vibe-code-security-scanner
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "vibe-code-security-scanner": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/vibe-code-security-scanner"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "vibe-code-security-scanner": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/vibe-code-security-scanner"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/vibe-code-security-scanner-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.05 per site scanned**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/vibe-code-security-scanner
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/vibe-code-security-scanner

*Findings come from the app's own public pages and client-side code.*
