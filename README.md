# Web Search Plus Homepage

Static landing page for [websearchplus.xyz](https://websearchplus.xyz/).

This page documents the Web Search Plus ecosystem:

- Hermes plugin: `robbyczgw-cla/hermes-web-search-plus`
- MCP server: `robbyczgw-cla/web-search-plus-mcp`
- OpenClaw Skill and Plugin variants

## Deploy

The site is deployed with Vercel as a static `index.html` project.

```bash
vercel --prod --yes
```

## Release checklist

When updating public package releases, keep these homepage markers aligned:

- Hermes plugin release links and install command
- MCP package version in `uvx --from web-search-plus-mcp==...`
- ClawHub Skill / OpenClaw Plugin versions where relevant
- Recent Updates section

No provider API keys or local runtime state belong in this repo.
