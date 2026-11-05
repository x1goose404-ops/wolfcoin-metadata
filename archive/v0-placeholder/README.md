# v0 placeholder archive (immutable)

This directory preserves the **original, pre-correction** Wolf Coin off-chain metadata
and artwork exactly as first published under the `v1` tag (commit
`0864ff54ba6f881faee4af8b61fecf9eebd5ddfe`).

It is kept for audit and rollback. **Do not edit these files.**

## What was wrong with v0
- `Denomination` = `1 XNT` (the on-chain collateral is **5 XNT**).
- `image` = `coin.png` — a 512x512 black-gold geometric placeholder glyph
  (sha256 `cad53cc22fba26ba1b5d8573562a9e322c148cbe7efef735ce7262375d62eca7`).
- No `Edition` attribute.

## Corrected content (v1, commit 131d14c27b8b8ba89f2582d4d429ed2a92325580)
- `Denomination` = `5 XNT`, `Edition` = `BETA TEST EDITION`, `image` = `coin.webp`.
- `coin.webp` = the sealed X1 Vault inscription (316,818 bytes,
  BLAKE3 `1c870487914dc51dab1d5edba988c399960a3f464faa3bf3cdb396ce9d3b8f7c`,
  sha256 `536833d6d16ecb38517767285b80578fc82da5d9f51425c2faf191ebcff2443f`).

## File hashes (sha256)
```
8a66ef50c476f4912a1824fbe51d6614605f501a2d226f1049e7e3c8be6e342f  10.json
f0c289795a4cc3f5a167691cfb6cbf537d039ce2d05a4cc6770adbb5da2a55fb  1.json
e41aeefbffcd07b56dc7ee8b22b2c51051e27543f11cc90548f5d30c673958dd  2.json
21b49baef56eece60fce934e736def5183a8c65bfe0b05878eacc6a76a693724  3.json
38e922d404d06f64aa90e4b1fe25258bce805bbff591bb9586bb45bb6245b2e3  4.json
7d1ac1dfbda41d3aa05894c716bfea559c98f8dc4a2e3fbd6d16ed3d5e6a952f  5.json
c4d67a4d77bdb77d1cf35aaee99392ffc1d5e1e83c349c36ba2fe076101d9a78  6.json
fb478cdf96d3016119aed8bf458f310da5c32599232b70992aefb412e4f03800  7.json
9ad541223e18502922524f228315a841af36b5947abe4a39582d66987a1bf975  8.json
7eba79f5771e89524df893f3368a7e09a35bebc371b023eea4a81265f9b53dd1  9.json
cad53cc22fba26ba1b5d8573562a9e322c148cbe7efef735ce7262375d62eca7  coin.png
```

## Rollback
The original commit is `0864ff54ba6f881faee4af8b61fecf9eebd5ddfe` (tag
`v0-original-0864ff5`). To roll the release tag back:
`git tag -f v1 0864ff5 && git push -f origin v1` (only if the corrected content must be withdrawn).
