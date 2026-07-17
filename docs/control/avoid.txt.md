---
title: avoid.txt
categories:
  - avoid
  - control
---

Kore has the ability to avoid certain players. If the option [avoidList](../config.txt/avoidList.md) in [config.txt](/cat/config.txt/) is enabled, you can list players in the file avoid.txt to make Kore automatically avoid certain players. Also in the **\[Jobs\]** section, you can list the professions that should be avoided. For example, it is known that priests most often pursue bots, they can heal a mob or hang up any status and watch the reaction of the bot.

Depending on how you set the corresponding options for each player in the list, Kore can either disconnect or teleport when a player in the avoid list is seen. You can also make Kore disconnect when you detect a chat message from a player in the list. The file **avoid.txt** has three sections: **\[Players\]**, **\[ID\]** and **\[Jobs\]**.

## Syntax

You specify player names that you want to avoid under the section **\[Players\]**. This section may contain one or more lines that observes the following syntax.

`<player_name> (TABs) <disconnect> <teleport\respawn> <disconnect_on_chat>`

The **\[ID\]** section is the same as the \[Players\] section, but you specify player IDs instead of player names. This is usually used to avoid GMs who have the ability to change their names. The \[ID\] section may contain one or more lines that observes the following syntax:

`<player_ID> (TABs) <disconnect> <teleport\respawn> <disconnect_on_chat>`

The professions of the players you want to avoid are listed in the **\[Jobs\]** section. This section appeared in :simple-github: [PR#2941](https://github.com/OpenKore/openkore/pull/2941). This section may contain one or two columns that correspond to the following syntax:

`<jobs_name> (TABs) <disconnect> <teleport\respawn>`

**Note:** if both actions are enabled for one entry (`<disconnect>` and `<teleport>`), then the bot will teleport first, then it will shut down for the time specified in the [avoidList_reconnect](../config.txt/avoidList_reconnect.md) parameter.

### Details
---

[`<player_name>`](../References.md#player_names)

This is the name of the player you want to avoid.

`<player_ID>`

This is the account ID of the player you want to avoid. You can obtain this value by using the [pl](../Console_Command/pl.md) console command if the player is nearby.

`<jobs_name>`

The name of the profession you want to avoid. The correct name can be found in the :simple-github: [src/Globals.pm](https://github.com/OpenKore/openkore/blob/master/src/Globals.pm#L180) file. For example, you can configure the bot to avoid all acolytes\\priests\\monks. Attention: in the [avoidList_ignoreList](config.txt/avoidList_ignoreList.md) config parameter, you can configure trusted players from which the bot will not hide. Do not forget to configure the options [ avoidList_inLockOnly 1](config.txt/avoidList_inLockOnly.md).

`<disconnect>`

This is a [boolean](../References.md#boolean_flag){ data-preview } that tells if Kore should disconnect when the player is seen on screen. When you disconnect due to avoiding players, Kore will reconnect after the number of seconds specified in the option [avoidList_reconnect](config.txt/avoidList_reconnect.md) in config.txt.

`<teleport\respawn>`

This flag tells if Kore should teleport away when the player is seen on screen. You must have the Teleport Skill or Fly Wings in inventory or this option will fail (see also [teleportAuto_useSkill](config.txt/teleportAuto_useSkill.md)).

| Value | Description                       |
|-------|-----------------------------------|
| 0     | Do not react                      |
| 1     | Teleport away                     |
| 2     | Teleport away and then disconnect |

`<disconnect_on_chat>`

This is a [boolean](../References.md#boolean_flag){ data-preview } that tells if Kore should disconnect when a chat message from the player is detected. When you disconnect due to avoiding players, Kore will reconnect after the number of seconds specified in the option [avoidList_reconnect](config.txt/avoidList_reconnect.md) in config.txt.

## Examples

If you know the names of the players you want to avoid, you can specify their names under the \[Players\] section as follows:

```
[Players]
Grand Master 1 0 0
Killer       0 0 1
Booya        0 1 1
```

In the example above, you will disconnect when "Grand Master" is in sight and when "Killer" or "Booya" sends you a chat message. You will also teleport when "Booya" is on sight. On the other hand, if you only know the player ID, place it under the \[ID\] section as follows:

```
[ID]
650874   1 0 1
```

The example above will make you disconnect whenever player #650874 is on screen, or when that player sends you a private message.

```
[Jobs]
Acolyte  0 1
Priest   0 1
```

The example above will cause the bot to teleport when some acolyte or prist appears on the screen.

!!! tip ""
    Category: [control](/cat/control)