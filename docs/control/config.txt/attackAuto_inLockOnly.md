---
title: attackAuto_inLockOnly
categories:
  - config.txt
  - config.txt|attack
  - fields
---

`attackAuto_inLockOnly` [`<flag>`](../../References.md#flag){ data-preview }<br>
`homunculus_attackAuto_inLockOnly` [`<flag>`](../../References.md#flag){ data-preview }<br>
`mercenary_attackAuto_inLockOnly` [`<flag>`](../../References.md#flag){ data-preview }

This options sets whether auto-attack will be disabled outside the [lockMap](lockMap.md).

| Flag | Description |
|----|----|
| 0 or blank | Attack monsters in any map. |
| 1 | Attack monsters on [lockMap](lockMap.md) and on route to it. |
| 2 or any greater value | Attack monsters only on [lockMap](lockMap.md). |

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack) | [fields](/cat/fields) | [homunculus](/cat/homunculus) | [mercenary](/cat/mercenary)