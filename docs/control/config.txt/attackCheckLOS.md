---
title: attackCheckLOS
categories:
    - config.txt
    - config.txt|attack
---

`attackCheckLOS` [`<boolean>`](../../References.md#boolean_flag){ data-preview }

This option toggles the use of LOS (Line Of Sight) check code when attacking.

If this option is enabled and you are a ranged attacker (i.e. [attackDistance](attackDistance.md) is set to a value greater than 2), this will check whether you have a clear line of sight to the target, if not, it will attempt to move to a space where you do while respecting [runFromTarget_dist](runFromTarget_dist.md) and [followDistanceMax](followDistanceMax.md).

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)