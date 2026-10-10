# scoop-bucket — TOTP Vault

Personal [Scoop](https://scoop.sh) bucket for
[TOTP Vault](https://github.com/spapas/totpvault)
(small offline TOTP authenticator, MIT-licensed).

## Install

```powershell
scoop bucket add totpvault https://github.com/spapas/scoop-bucket
scoop install totpvault
```

## Update

```powershell
scoop update totpvault
```

## Maintainer notes

On each `totpvault` release, bump `bucket/totpvault.json`:
`version`, `architecture.64bit.url` and `architecture.64bit.hash`
(hash from the release `SHA256SUMS`). `checkver`/`autoupdate` follow the
same `totpvault-v$version-windows-amd64.zip` asset naming — keep
`scripts/package_release.py` stable.
