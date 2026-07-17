---
title: attackAuto_party
categories:
- config.txt|attack
---

`attackAuto_party` [`<flag>`](../../References.md#flag){ data-preview }

This option sets whether Kore should attack monsters engaged by party members.

| Flag      | Description                                                    |
|------------|----------------------------------------------------------------|
| 0 or empty | Do nothing.                                                    |
| 1          | Attack monsters, already engaged in fight with your party.     |
| 2          | Attack monsters only if they have started attacking the party. |

!!! Notes
    - Use the flag value **2** if you are being tanked to prevent you from laying the attack to the monster first while the monster is still moving towards your tanker. Unless those monsters are known to have a habit of switching targets regardless of who made the first attack, this flag ensures that monsters will always attack the party/tanker.
    - This option works independently from [attackAuto](attackAuto.md), thus if this option is enabled, you will attack monsters engaged by your party regardless of how attackAuto is set.
    - Kore will only attack monsters engaged by the follow target if there are no other aggressive monsters attacking Kore itself. If you want to give priority on monsters engaged by your party, set [attackAuto](attackAuto.md) to **0**.

    --8<-- "template/OnlyWhenAiAuto.md"

!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)