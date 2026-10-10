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

On each `totpvault` release, bump `bucket/totpvault.json`:
`version`, `architecture.64bit.url` and `architecture.64bit.hash`
(hash from the release `SHA256SUMS`). `checkver`/`autoupdate` follow the
same `totpvault-v$version-windows-amd64.zip` asset naming — keep
`scripts/package_release.py` stable.

On each `workmail-mcp` release, bump `bucket/workmail-mcp.json` the same
way (`version`, `architecture.64bit.url`, `architecture.64bit.hash` from
`workmail-mcp-windows-amd64.exe.sha256`), or run
`scoop update workmail-mcp` and let `autoupdate` refresh the hash —
it follows the `workmail-mcp-windows-amd64.exe` asset naming, so keep
the release workflow asset names stable.
