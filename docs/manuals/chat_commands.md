---
title: Chat_commands
categories:
  - TODO
---

Kore allows authorized players to issue commands by using messages in private, party or guild chat. This way, you can play using another account and still be able to control your bot.

## Authorization

Before you are allowed to use Chat Commands, Kore must recognize you as authorized or it will just ignore your commands. There are two ways to give authorizization to a player:

1. by using the console command [auth](../console_command/auth.md) specifying the name of the player to authorize, or
2. by sending Kore a private message that contains the [adminPassword](../control/config.txt/adminPassword.md) set in its [config.txt](/cat/config.txt) (only if [inGameAuth](../control/config.txt/inGameAuth.md) is enabled).

## Callsign

You can send chat commands directly to Kore by using private messages, however, issuing commands in party or guild chat is different. When using party or guild chat, you need to include in your message the [callSign](../control/config.txt/callSign.md) set in its [config.txt](/cat/config.txt). For example, if Kore has "Slave" as its callsign, you would use the following command to make it follow you around:

!!! Example
    `Slave follow`

The callsign is not case-sensitive and it can appear anywhere in the message, but only once.

!!! Example
    `conf attackAuto slave`

Note however, that while the callsign can appear anywhere, the command itself must follow the proper syntax and the arguments must appear in the correct order. Avoid unnecessary punctuations.

## Command List

### `agi`

Tell Kore to use Increase AGI on a player.

!!! info "Syntax"
    ```
    agi [ me | <player_name> ]
    ```

`<player_name>` - a partial name of a player within Kore\'s immediate area.

Command | Description
------- | -----------
`agi`<br>`agi me` | Use Increase AGI on the player who issued the chat command.
`agi <player_name>` | Use Increase AGI on the player whose name matches the specified partial name.

---

### `bless`

Tell Kore to use Blessing on a player.

!!! info "Syntax"
    ```
    bless [ me | <player_name> ]
    blessing [ me | <player_name> ]
    ```

`<player_name>` - a partial name of a player within Kore's immediate area.

Command | Description
------- | -----------
`bless`<br>`bless me`<br>`blessing`<br>`blessing me` | Use Blessing on the player who issued the chat command.
`bless <player_name>`<br>`blessing <player_name>` | Use Blessing on the player whose name matches the specified partial name.

---

### `conf`

Change a configuration key.

!!! info "Syntax"
    ```
    conf <config_key> [ <value> | none ]
    conf <label_name>.( <attribute> | block ) [ <value> | none ]
    ```

`<config_key>` - a configuration key name from [config.txt](/cat/config.txt).

`<value>` - any value depending on the configuration key being changed.

`<label_name>.<attribute>` - by specified label name in configuration block, you can use label name instead of configuration key.

Command | Description
------- | -----------
`conf <config_key>` | Display the current value of the specified configuration key.
`conf <config_key> <value>` | Set a new value for the specified configuration key.
`conf <config_key> none` | Unset the specified configuration key.
`conf <label_name>.<attribute>` | Display the current value of the specified attribute.
`conf <label_name>.<attribute> <value>` | Set a new value for the specified attribute.
`conf <label_name>.<attribute> none` | Unset the specified attribute.

!!! example
    ```
    conf lockMap ptr_fild08
    conf lockMap none
    conf useHP.disabled 1
    conf applesEtc.block Meat
    ```

!!! note
    Kore will not disclose the username and password using this command.

---

### `date`

Ask Kore for the current date and time.

---

### `follow`

Tell Kore to follow a player.

!!! info "Syntax"
    ```
    follow [ me | <player_name> | stop ]
    ```

`<player_name>` - a partial name of a player within Kore\'s immediate area.

Command | Description
------- | -----------
`follow`<br>`follow me` | Follow the player who issued the chat command.
`follow <player_name>` | Follow the player whose name matches the specified partial name.
`follow stop` | Stop following.

---

### `heal`

Tell Kore to use Heal on a player.

!!! info "Syntax"
    ```
    heal [ me | <player_name>] ( <amount_hp> )
    heal ( <amount_hp> ) [ me | <player_name> ]
    ```

`<player_name>` - a partial name of a player within Kore\'s immediate area.

`<amount_hp>` - the amount of hp that will be healed.

Command | Description
------- | -----------
`heal <amount_hp>`<br>`heal <amount_hp> me`<br>`heal me <amount_hp>` | Use Heal on the player who issued the chat command.
`heal <player_name> <amount_hp>`<br>`heal <amount_hp> <player_name>` | Use Heal on the player whose name matches the specified partial name.

---

### `kyrie`

Tell Kore to use Kyrie Eleison on a player.

!!! info "Syntax"
    ```
    kyrie [ me | <player_name> ]
    ```

`<player_name>` - a partial name of a player within Kore\'s immediate area.

Command | Description
------- | -----------
`kyrie`<br>`kyrie me` | Use Kyrie Eleison on the player who issued the chat command.
`kyrie <player_name>` | Use Kyrie Eleison on the player whose name matches the specified partial name.

---

### `logout`

Tell Kore to quit.

---

### `look`

Tell Kore to look in a certain direction. See similar console command look for the list of values for body and head directions.

!!! info "Syntax"
    ```
    look ( <body_dir> ) [ <head_dir> ]
    ```

TODO: examples need to be added

---

### `mag`

Tell Kore to use Magnificat.

---

### `move`

Tell Kore to move.

!!! info "Syntax"
    ```
    move ( <x> <y> ) [<map_name>]
    move ( <map_name> ) [<x> <y>]
    move stop
    ```

`<x>` - x-coordinate.

`<y>` - y-coordinate.

`<map_name>` - the name of a map as shown by the where command in Kore, or the `/where` command in the Ragnarok Online client (e.g. prontera, morocc, prt_fild08, etc.).


Command | Description
------- | -----------
`move <x> <y>` | Move to the specified coordinates on the current map.
`move <map_name>` | Move to the specified map.
`move <x> <y> <map_name>`<br>`move <map_name> <x> <y>` | Move to the specified coordinates on the map.
`move stop` | Stop all movements.

---

### `reload`

Reload configuration and table files.

!!! info "Syntax"
    ```
    reload ( all | <names> ) [ except <names> ]
    ```

`<names>` - a list of words that match config and table filenames.

Command | Description
------- | -----------
`reload all` | Reload all configuration and table files.
`reload <names>` | Reload config and table files that match the specified list of names.
`reload <names> except <names>` | Reload config and table files that match the first specified list of names except those that match the list of names after the except keyword.
`reload all except <names>` | Reload all config and table files except those that match the specified list of names.

!!! example
    The following example will reload all config files inside the 'control' folder:
    ```
    reload control
    ```
    
    The next example will reload all table files inside the 'tables' folder except for `tables\itemsdescriptions.txt`, `tables\portals.txt`, `tables\portalsLOS.txt` and `tables\skillsdescriptions.txt`:
    ```
    reload tables except itemsdesc portals skillsdesc
    ```

---

### `relog`

Tell Kore to log out then log in again.

!!! info "Syntax"
    ```
    relog [ <seconds> ]
    ```

`<seconds>` - the time in seconds.

Command | Description
------- | -----------
`relog` | Logout and then login after 5 seconds.
`relog <seconds>` | Logout and then login after the specified number of seconds.

---

### `shut up`

Tell Kore to turn verbose off. Kore will not reply to chat commands when verbose is off.

---

### `sit`

Tell Kore to sit.

!!! note
    To ensure that Kore will stay put, this command will set the [config.txt](/cat/config.txt) option [`attackAuto`](../control/config.txt/attackAuto.md) to **1**, and the options [`attackAuto_party`](../control/config.txt/attackAuto_party.md), [`route_randomWalk`](../control/config.txt/route_randomWalk.md), [`teleportAuto_idle`](../control/config.txt/teleportAuto_idle.md), and [`itemsGatherAuto`](../control/config.txt/itemsGatherAuto.md) to **0**. The original values are stored so they can be reset when the stand command is used.

---

### `speak`

Tell Kore to turn verbose on. Kore will reply to chat commands when verbose is on.

---

### `stand`

Tell Kore to stand.

!!! note
    If you previously used the sit command to force Kore to sit, this will set the [config.txt](/cat/config.txt) options [`attackAuto`](../control/config.txt/attackAuto.md), [`attackAuto_party`](../control/config.txt/attackAuto_party.md), [`route_randomWalk`](../control/config.txt/route_randomWalk.md), [`teleportAuto_idle`](../control/config.txt/teleportAuto_idle.md), and [`itemsGatherAuto`](../control/config.txt/itemsGatherAuto.md) to their original values.

---

### `status`

Ask Kore for status information (HP, SP, base and job levels, base and job experiences, weight, and zeny).

---

### `stop`

Tell Kore to stop all movements.

---

### `tank`

Tell Kore to tank for a player.

!!! info "Syntax"
    ```
    tank [ me | <player_name> | stop ]
    ```

`<player_name>` - a partial name of a player within Kore\'s immediate area.

Command | Description
------- | -----------
`tank`<br>`tank me` | Start tanking for the player who issued the chat command.
`tank <player_name>` | Start tanking the player whose name matches the specified partial name.
`tank stop` | Stop tank mode.

---

### `thank`

Thank Kore for a job well done. ^_^

!!! info "Syntax"
    ```
    thank | tnh | thx
    ```

!!! note
    Kore will only reply to this chat command if the number of seconds set in [`ai_thanks_set`](../Feature_Request/timeouts.txt.md#ai-thanks) in [timeouts.txt](../Feature_Request/timeouts.txt.md) has not yet elapsed since the last chat command succeeded.

----

### `timeout`

Set Kore's timeouts.

!!! info "Syntax"
    ```
    timeout <timeout> [ <seconds> ]
    ```

`<timeout>` - a timeout key name from [timeouts.txt](../Feature_Request/timeouts.txt.md).

`<seconds>` - the time in seconds.

Command | Description
------- | -----------
`timeout <timeout>` | Display the current value of specified key name.
`timeout <timeout> <seconds>` | Set a new value for the specified key name.

---

### `town`

Tell Kore to respawn back to the save point.

!!! note
    Unless Kore is dead, it needs a Butterfly Wing in inventory, or the Teleport Skill, to respawn.

---

### `where`

Ask Kore for its current location.
