# scoop-bucket — TOTP Vault + workmail-mcp

Personal [Scoop](https://scoop.sh) bucket for
[TOTP Vault](https://github.com/spapas/totpvault)
(small offline TOTP authenticator, MIT-licensed) and
[workmail-mcp](https://github.com/spapas/workmail-mcp)
(local IMAP-to-MCP bridge, MIT-licensed).

## Install

```powershell
scoop bucket add spapas https://github.com/spapas/scoop-bucket
scoop install totpvault
scoop install workmail-mcp
```

## Update

```powershell
scoop update totpvault
scoop update workmail-mcp
```

## Maintainer notes

`bucket/totpvault.json` and `bucket/workmail-mcp.json` carry `checkver`/
`autoupdate` metadata and are bumped automatically by the `Excavator`
workflow (`.github/workflows/excavator.yml`, every 4 hours + manual dispatch).
Manual bumps are only needed to fast-track a release — copy `version`, URL and
hash from the release assets (`SHA256SUMS` for totpvault,
`workmail-mcp-windows-amd64.exe.sha256` for workmail-mcp).
