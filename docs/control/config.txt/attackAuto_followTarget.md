---
title: attackAuto_followTarget
categories:
  - config.txt
  - config.txt|attack
---

`attackAuto_followTarget` [`<boolean>`](../../References.md#boolean_flag){ data-preview }

If Kore is [following a player](follow.md) and this option is set to **1**, Kore will attack monsters that are engaged by its [followTarget](followTarget.md).

!!! note
    - This option works independently from [attackAuto](attackAuto.md), thus if this option is enabled, you will attack monsters engaged by the follow target regardless of how attackAuto is set.
    - Kore will only attack monsters engaged by the follow target if there are no other aggressive monsters attacking Kore itself. If you want to give priority on monsters engaged by the follow target, set [attackAuto](attackAuto.md) to **0**.
    
    --8<-- "template/OnlyWhenAiAuto.md"

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)