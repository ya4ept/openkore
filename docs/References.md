---
title: References
---
<style>
  .md-sidebar--primary {
    display: block !important;
  }
</style>

## Syntax Legends
Syntax format used in declarations of configuration options and commands.

| Symbol | Description |
|--------|-------------|
| **Bold** | Elements that the user must type exactly as shown. |
| `< >` | Information that the user must specify. |
| `( )` | Required parameters. |
| `[ ]` | Optional parameters. |
| `|` | Means OR. This separates choices from which the user must choose only one. |

## Basic Value and Parameter Types
Parameters types that may appear in a configuration option\'s value or a command parameter.

### boolean flag

Option values are interpreted with [Perl's Truth and Falsehood](https://perldoc.perl.org/5.12.5/perlsyn#Truth-and-Falsehood) rules.

| Value                            | Description     |
|----------------------------------|-----------------|
| 0 or empty string (unset option) | FALSE (disable) |
| 1                                | TRUE (enable)   |

Actually, [boolean flag](https://perldoc.perl.org/5.12.5/perlsyn#Truth-and-Falsehood) (which isn't checked for anything but boolean) can have any value.

Boolean options MAY be extended in future. In such a case, values of **0** and **1** SHOULD preserve the old behaviour, and more values MAY be added.

**API:** There is no special API, just usual Perl logical operators are used.

!!! Example
    `if ($config{useDeadlyRay}) { ...`

---

### flag

A number with special meaning on its current context. The list of meaningful values are always given.

---

### number

A number with special meaning on its current context. The list of meaningful values are always given. May be a fractional value (with dot `.` separator) or just an integer. Empty string (unset option) or strings starting with non-numeric characters are evaluated as in Perl, usually to **0**.

!!! Notes
    This is not a [range](#range_operators). Values like `= 11` would just evaluate to **0**.

**API:** There is no special API, just usual [Perl's relational and equality operators](https://perldoc.perl.org/perlop.html#Relational-Operators) are used.

!!! Example
    `if ($config{answerToLifeUniverseAndEverything} == 42) { ...`

---

### percent

A number from 1 to 100 that corresponds to a percent. Don't append a percent sign (%) unless otherwise specified.

---

### seconds

The time specified in seconds. Can be a fractional value (ex. 0.5).

---

### string

Any text string.

---

## Equipment Slots

Equipment slot names used by Openkore.

| Name           | Description               |
|----------------|---------------------------|
| topHead        | Upper head slot.          |
| midHead        | Middle head slot.         |
| lowHead        | Lower heads slot.         |
| rightHand      | Right hand slot.          |
| leftHand       | Left hand slot.           |
| rightAcessory  | Right Acessory slot.      |
| leftAcessory   | Left Acessory slot.       |
| armor          | Armor slot.               |
| robe           | Gaments slot.             |
| shoes          | Footwear slot.            |
| costumeTopHead | Upper head costume slot.  |
| costumeMidHead | Middle head costume slot. |
| costumeLowHead | Lower heads costume slot. |
| costumeRobe    | Robe costume slot.        |
| costumeFloor   | Floor costume slot.       |
| arrow          | Arrow or Bullet slot.     |

!!! Notes "Developer Notes:"
    Equipment slot names are defined in :simple-github: [%Globals::equipSlot_lut](https://github.com/OpenKore/openkore/blob/master/src/Globals.pm#L61).

---

## Message Domains

Message domains are names used to classify messages printed in the console.

For information about a certain messages that you see in your console, set the option [showDomain](control/config.txt/showDomain.md) in [config.txt](cat/config.txt.md) to **1**, making Openkore display domains along with messages in the console.

### List of Message Domains

| Name                | Description                            |
|---------------------|----------------------------------------|
| ai_attack           | Attack messages                        |
| ai_npcTalk          | NPC talk sequence messages.            |
| attacked            | Monster attacks you.                   |
| attackedMiss        | Monster attacks you but misses.        |
| attackMon           | You attack monster.                    |
| attackMonMiss       | You attack monster but misses.         |
| connection          | Connection messages.                   |
| console             | Messages without defined group.        |
| deal                | Deal messages.                         |
| devotion            | Devotion messages.                     |
| drop                | Monster drop related messages.         |
| emotion             | Emoticon messages.                     |
| exp                 | Experience gained message.             |
| equip               | Equipment switching message.           |
| follow              | Follow messages.                       |
| guildchat           | Guild chat message.                    |
| guildnotice         | Guild notice message.                  |
| info                | Character information messages.        |
| input               | User input messages.                   |
| inventory           | Inventory related messages.            |
| list                | Actor\'s list message.                 |
| load                | Loading config files messages.         |
| looter              | Attacking looter message.              |
| map_event           | PvP/GvG mode messages.                 |
| npc                 | NPC messages.                          |
| parseMsg_statuslook | Changed status/equipment messages.     |
| parseMsg/hairColor  | Hair color change message.             |
| parseMsg/job        | Job change message.                    |
| parseMsg/upgrade    | Item upgrading message.                |
| party               | Party/follow related message.          |
| partychat           | Party chat messages.                   |
| pet                 | Pet related messages.                  |
| plugins             | Plugin handle messages.                |
| pm                  | Received private messages.             |
| pm/sent             | Sent private messages.                 |
| portals             | Portal existance messages.             |
| portalRecord        | Recording of portals messages.         |
| publicchat          | Public chat message.                   |
| refine              | Weapon refining messages.              |
| route               | Routing/pathfinding messages.          |
| route_teleport      | Route teleport messages.               |
| schat               | GM broadcast messages.                 |
| selfSkill           | Skills used by yourself messages.      |
| skill               | Skills not related to attack messages. |
| sold                | Items sold while vending messages.     |
| startup             | Startup messages.                      |
| storage             | Storage item added/removed messages.   |
| success             | Operation succeeded messages.          |
| syntax              | Syntax check files messages.           |
| teleport            | Teleporting messages.                  |
| useItem             | Items used by you messages.            |
| useTeleport         | Attemp to use teleport messages.       |
| waypoint            | Waypoint messages.                     |
| xkore               | X-Kore system messages.                |

### List of Debug Domains

- ai
- ai_attack
- ai_autoCart
- ai_makeItem
- ai_move
- ai_npcTalk
- attackMonMiss
- autoBreakTime
- connection
- d_sendPacket
- debug
- drop
- equipAuto
- guild
- ipc
- Item
- monsterSkill
- npc
- packetParser
- parseInput
- parseMsg
- parseMsg_comboDelay
- parseMsg_damage
- parseMsg_move
- parseMsg_presence
- parseMsg_presence/name
- parseMsg_presence/player
- parseMsg_presence/remote
- parseMsg_statuslook
- parseSendMsg
- pet
- route
- route_teleport
- sendPacket
- sitAuto
- skill
- storage
- useTeleport
- vending

---

## AI Queue

List of possible AI states:

| Name | AI state description |
|----|----|
| attack | OpenKore is attacking someone |
| autoResponse | OpenKore automatically replies to chat messages (see [autoResponse](control/config.txt/autoResponse.md)) |
| buyAuto | OpenKore has initiated automatic item purchase (see [buyAuto](control/config.txt/buyAuto.md)) |
| cartAdd | OpenKore moves items to [cart](console_command/cart.md) |
| cartGet | OpenKore gets items from the [cart](console_command/cart.md) |
| clientSuspend | AI is frozen, for example after changing the map |
| dead | Char died |
| deal | OpenKore makes [deal](console_command/deal.md) |
| drop | OpenKore throws items (see [drop](console_command/drop.md)) |
| equip | OpenKore [equips](../Skill_Use_Condition/equip.md) items |
| escape | Openkore tries to [escape from unknown map](control/config.txt/route_escape_reachedNoPortal.md) |
| follow | OpenKore [follows](control/config.txt/follow.md) another player |
| items_gather | Openkore picks up other people\'s items from the ground (see [itemsGatherAuto](control/config.txt/itemsGatherAuto.md)) |
| items_take | OpenKore picks up items after killing a monster (see [itemsTakeAuto](control/config.txt/itemsTakeAuto.md)) |
| look | OpenKore is [looking](console_command/look.md) in the indicated direction |
| move | OpenKore moves to the specified coordinates within the line of sight |
| NPC | OpenKore [talking](console_command/talk.md) to NPC |
| route | OpenKore moves to the specified point using pathfinding. |
| sellAuto | OpenKore has initiated automatic selling of items (see [sellAuto](control/config.txt/sellAuto.md)) |
| sendEmotion | OpenKore sends an emote |
| sitAuto | OpenKore automatically sits down (see [:Category:sitting](../Category/sitting.md)) |
| sitting | OpenKore sits down |
| skill_use | OpenKore uses skill |
| standing | OpenKore stands up |
| storageAuto | OpenKore has initiated automatic stocking of items (see [storageAuto](control/config.txt/storageAuto.md)) |
| take | OpenKore picks up items after killing a monster (see [itemsTakeAuto](control/config.txt/itemsTakeAuto.md)) TODO: hat is the difference between \"items_take\" and \"take\"? |
| teleport | OpenKore uses [teleport](console_command/tele.md) or [respawn](console_command/respawn.md) |
| transferItems | OpenKore moves items from one location (inventory/cart/warehouse) to another |

---

## Names

Sometimes equipment/item/monster names are different in each server, so Openkore have it's own database in tables folder for defaulting names. Changing the name from the files will affect your configuration.

### Equipment names

Openkore equipment name syntax:

```
# for normal equipments:
[BROKEN] [+<upgrade_level>] <item_name> [[<card_name>[*<number>]] [<number_of_slots>]]

# for elemental weapons:
[BROKEN] [+<upgrade_level>] [VS|VVS|VVVS][Fire|Earth|Wind|Water] <item_name>
```

!!! Notes
    - If the equipment is not broken, omit the **`BROKEN`** part.
    - If the equipment is not upgraded, omit the **`+<upgrade_level>`** part.
    - Use only the monster name for the `<card_name>`, e.g. use "Hydra" for the "Hydra Card".
    - If there is only one card of a certain type slotted on the equipment, omit the **`*<number>`** part.
    - If there are more than one type of cards compounded on the equipment, the **`<card_name>*<number>`** pair should be colon-separated list. The list should be sorted alphabetically.
    - If the equipment is not slotted, omit the **`[<number of slots>]`** part.
    - So far configuration options using item names are not strict with case-sensitivity.
    - If you have the equipment, you can use [console commands](/cat/console-command/)

??? Example
    +7 Cranial Mirror Shield:
    ```
    +7 Mirror Shield [Thara Frog] [1]
    ```
    Hard Padded Armor:
    ```
    Padded Armor [Pupa] [1]
    ```

    3-slotted +5 Double Flammable Boned Sabe:
    ```
    +5 Saber [Skel Worker:Vadon*2] [3]
    ```

    +6 Very Very Strong Wind Tsurug:
    ```
    +6 VVS Wind Tsurugi
    ```

---

### Item names

Item names can be found at `tables\items.txt`, following this syntax:

```
<Item_ID>#<item_name>#
```

In items.txt item names are separated with underscores (\_), to use them in your configuration replace them with spaces.

!!! Example
    Item's name is Mirror Shield:
    ```
    2107#Mirror_Shield#
    ```

!!! Note
    - So far configuration options using item names are not strict with case-sensitivity.
    - You can also get item's name by using [console commands](/cat/console-command/), like [`i`](console_command/i.md), [`cart`](console_command/cart.md), [`storage`](console_command/storage.md).

---

### Ground spell names

Ground spell names can be found at `tables\spells.txt`, following this syntax:

```
<Spell_ID> <spell_name>
```

!!! Example
    Ground spell name: Safety Wall:
    ```
    126 Safety Wall
    ```

!!! Note
    Ground spell names can also be found using [console command](/cat/console-command/) [`spells`](console_command/spells.md) while certain spells are active on the ground.

---

### Map names

Map names can be found at `tables\maps.txt`, following this syntax:

```
<map_file_name>#<map_name>#
```

Openkore use just the first name of the map in it's configuration files.

!!! Example
    Map name is Prontera:
    ```
    prontera.rsw#Prontera City#
    ```

!!! Notes
    Map names can also be find using [console command](/cat/console-command/) [`where`](console_command/where.md).

---

### Monster names

Monster names can be found at `tables\monsters.txt`, following this syntax:

```
<monster_ID> <monster_name>
```

!!! Example
    Monster name is Scorpion:
    ```
    1001 Scorpion
    ```

!!! Notes
    You can also find monster name using [console command](/cat/console-command/) [`ml`](console_command/ml.md) while certain monters are on screen.

---

### Player names

Player names can be found by using the [console command](/cat/console-command/) [`pl`](console_command/pl.md) while certain players are on screen.

!!! Note
    These are case-sensitive.

---

### Skills names

In OpenKore configs, in macros or when using console commands, sometimes you have to specify skills. When writing a skill, you can use three equivalent options:

1. `<skill_ID>` - unique skill number. Does not depend on OpenKore language settings. Can be found in [tables](../Category/tables.md)\\[SKILL_id_handle.txt](../tables/SKILL_id_handle.txt.md)
2. `<skill_handle>` - skill name (does not contain spaces). Does not depend on OpenKore language settings. Can be found in [tables](../Category/tables.md)\\[SKILL_id_handle.txt](../tables/SKILL_id_handle.txt.md) and [tables](../Category/tables.md)\\..\\[skillnametable.txt](../tables/skillnametable.txt.md)
3. `<skill_name>` - "human" name of the skill. Depends on OpenKore language settings. Can be found in the file [tables](../Category/tables.md)\\..\\[skillnametable.txt](../tables/skillnametable.txt.md)

!!! Example
    - 142 - skill_ID
    - NV_FIRSTAID - skill_handle
    - "First Aid" - English name of the skill
    - "Первая помощь" - Russian name of the skill

Currently used skill names can also be found by inspecting [`skills`](console_command/skills.md), [`homun skills`](console_command/homun.md), [`merc skills`](console_command/merc.md) commands output.

---

### Status names

Status handles (locale independent) can be found at `tables/{AILMENT,LOOK,STATE,STATUS}_id_handle.txt`.

Corresponding status names (depend on your configuration) can be found at `statusnametable.txt` used by your configuration.

Currently used status names can also be found by inspecting Kore output when certain status is received or by using the [`s`](console_command/s.md) command while certain status are active on you character.

---

## [NPC conversation codes](../Reference/NPC_conversation_codes.md)
`TODO`

---

## Range operators

User-specified [interval](https://en.wikipedia.org/wiki/Interval_(mathematics) "interval") for an option.

Value | Description
----- | -----------
X     | `{X}`
X..Y<br>X-Y | `[X, Y]`
> X  | `(X, +∞)`
>= X | `[X, +∞)`
< X  | `(-∞, X)`
<= X | `(-∞, X]`

!!! API
    Features and plugins MUST use :simple-github: [`Utils::inRange(<current_value>, <option_contents>)`](https://github.com/OpenKore/openkore/blob/master/src/Utils.pm#L1483) to check any kind of options with range values.

---

## [Self Conditions](../Category/Self_Condition.md)
<!-- TODO: шаблон {{:Category:Self Condition}} -->

## Target Conditions

### [Monster Conditions](../Category/Monster_Condition.md)
<!-- TODO: шаблон {{:Category:Monster Condition}} -->

### [Player Conditions](../Category/Player_Condition.md)
<!-- TODO: шаблон {{:Category:Player Condition}} -->

### [Skill Use Conditions](../Category/Skill_Use_Condition.md)
<!-- TODO: шаблон {{:Category:Skill Use Condition}} -->

### [Idle Condition](../Category/Idle_Condition.md)
<!-- TODO: шаблон {{:Category:Idle Condition}} -->

## [Interfaces](../Category/Interfaces.md)
<!-- TODO: шаблон {{:Category:Interfaces}} -->
