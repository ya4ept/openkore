---
title: attackBeyondMaxDistance_waitForAgressive
categories:
    - config.txt
    - config.txt|attack
---

`attackBeyondMaxDistance_waitForAgressive` [`<boolean>`](../../References.md#boolean_flag){ data-preview }<br>
`homunculus_attackBeyondMaxDistance_waitForAgressive` [`<boolean>`](../../References.md#boolean_flag){ data-preview }<br>
`mercenary_attackBeyondMaxDistance_waitForAgressive` [`<boolean>`](../../References.md#boolean_flag){ data-preview }

This config setting determines how openkore behaves when a ranged character has already damaged to their target, but the target is currently out of range.

If this parameter is **0** (old behavior), then openkore will move towards the monster.

If this parameter is set to **1** (new behavior), then openkore will wait in place until the wounded monster comes closer.

Appeared in :simple-github: [PR#3628](https://github.com/OpenKore/openkore/pull/3628)

!!! Note
    The following attack keys are meant to work only in private server (rAthena/Hercules). If you enable this in a official server you character will act weird, because character can't attack beyond the range.

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack) | [homunculus](/cat/homunculus) | [mercenary](/cat/mercenary)