# forcebi-claude-plugin

ForceBI MCP server for Claude, deployed at https://mcp.forcetechai.com

This repository is the Force Tech plugin marketplace for Claude. It has one plugin, `forcebi`: read-only ForceBI business data, limited to your own ForceBI login, company and permissions.

## Contents

- `.claude-plugin/marketplace.json`: the marketplace list (`forcetech`).
- `forcebi/`: the plugin. See [forcebi/README.md](forcebi/README.md) for setup, the read-only scope, privacy, support and uninstall.
  - `forcebi/.mcp.json`: the ForceBI connector, `https://mcp.forcetechai.com/mcp`.
  - `forcebi/skills/forcebi-answer/SKILL.md`: the ForceBI answer style and data rules.

## Install

Install ForceBI from the Claude directory in claude.ai, then click **Connect** and enter your company code. The connector login works in claude.ai only (see "Claude Code" in [forcebi/README.md](forcebi/README.md)).

## Support and privacy

- Support: support@forcetechai.com
- Privacy policy: https://www.forcetechai.com/privacy/

Copyright Force Tech Sdn Bhd (202501003410).
