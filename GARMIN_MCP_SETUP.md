# Garmin MCP setup

Uses [Taxuspt/garmin_mcp](https://github.com/Taxuspt/garmin_mcp). The server is declared in `.mcp.json`; it reads saved OAuth tokens, so no credentials live in this repo.

## One-time authentication (on your own machine)

```bash
uvx --python 3.12 --from git+https://github.com/Taxuspt/garmin_mcp garmin-mcp-auth
```

Enter your Garmin email, password and MFA code when prompted. Tokens are saved to `~/.garminconnect` (valid ~6 months; re-run with `--force-reauth`).
Check with `garmin-mcp-auth --verify` / `--diagnose`.

Then start Claude Code in this repo and approve the `garmin` server.
