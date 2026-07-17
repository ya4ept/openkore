---
title: attackAuto
permalink: /attackAuto/
tags:
- attack
- config.txt
categories:
    - config.txt
    - config.txt|attack
---

`attackAuto` [`<flag>`](../../References.md#flag){ data-preview }

Determines auto attack behavior.

| Flag | Description |
| :---: | ----------- |
| -1 | Do not automatically attack any monsters for any reason, even if they kill you. This setting is best for priests and other support characters who should never attack. It will allow them to act like players, running past monsters and ignoring any hits from the monsters. |
| 0 | Do not attack any monsters unless they attack you first. (Act like passive monsters.) |
| 1 | Attack monsters, already engaged in fight with you, [your master](attackAuto_followTarget.md) or [your party](attackAuto_party.md). (Act like "assist" monsters.) |
| \>= 2 | Aggressively attack monsters (without killsteal). (Act like aggressive monsters.) |

!!! notes
    --8<-- "template/OnlyWhenAiAuto.md"
    If no appropriate monsters found, the next check will be performed after [ai_attack_auto](timeouts.txt.md#ai_attack) seconds.

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)