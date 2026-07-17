---
title: arrowcraft.txt
categories:
  - control
---

If you have the Arrow Crafting Skill, Kore can automatically craft arrows for you. If the option [autoMakeArrows](../config.txt/autoMakeArrows.md) in [config.txt](../../cat/config.txt) is enabled, you can list items in the file arrowcraft.txt to make Kore automatically create arrows using the specified items.

## Syntax

The format of this file is simply a set of lines that observes the following syntax:

`<item_name> <use_flag>`

### Details

[`<item_name>`](../References.md#item_names)

Using the Arrow Crafting Skill, different type of arrows can be created from different ingredients. This value specifies the name of the item that you want to use as an ingredient when creating arrows.

`<use_flag>`

This is a [boolean](../References.md#boolean_flag) that specifies whether the item will be used to create certain arrows.

!!! Example
    This will allow Kore to create Fire Arrows and Iron Arrows from Red Blood and Garlet, respectively:

    ```
    Red Blood 1
    Garlet 1
    ```

!!! tip ""
    Category: [control](/cat/control)