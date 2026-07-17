---
title: config.txt
permalink: /Category:config.txt/
categories:
  - control
---

The file config.txt is the main configuration file. It is where you configure most of Kore's behavior.

## Syntax
Entries in this file follows two distict formats, the key-value and the block format. 

### Key-value format
The key-value format is outright simple. Each line contains a configuration key as the first word, followed by the value:

`<config_key> <value>`

### Block format
The block format, on the other hand, follows the similar concept, but additional attributes enclosed in curly brackets "{ }" extend the block config option's meaning:

```json
<сonfig_key> <value> {
	<attribute1> <value1>
	<attribute2> <value2>
}
```

These formats are strict. You can't use many options in one line. Curly brackets must be positioned exactly as in the example.

## Details

###`<config_key>`

This is one of the configuration variable names used by Kore. See the configuration list below for a list of available config variables.

### `<value>`

This sets the value for the corresponding configuration variable that will be used by Kore. The type of meaningful values vary with each configuration key. The proper values for each config keys are described in the configuration list below.

###`<attribute>`

These are basically the same as config keys but they are only used inside configuration blocks. These attributes define properties for the current block, as well as the conditions when the block will be used.

Note: Lines that begin with the pound sign (#) are comment lines. They are ignored by Openkore. You can also make blocks of comments by enclosing multiple lines inside `/*` and `*/`.

## Notes

Most of the configuration settings in this file are optional. Unless otherwise specified, you can either leave the value empty or delete the whole entry, in which case either the default value will be used (e.g disabled for boolean flags) or the option will be completely ignored.

Each unique configuration key in key-value lines must appear only once inside this file (except for [!include](!include.md){ data-preview }. When multiple lines have the same config key, that configuration option takes the value set in the line that appears last.

In contrast, you can specify an unlimited number of blocks with the same configuration key name. However, not all blocks defined for a certain configuration key will always be used by Kore. When Kore is ready to use a certain type of block configuration, Kore checks each defined block from top to bottom and stops when it finds a block whose defined attributes or conditions are met. Therefore, place the more important block options on top and the lower priority ones, below.

## Developer Notes

Empty by default options which are rarely needed shouldn't be added to default config. New users would be confused by them, and power users can discover them by reading this manual or source code.

!!! tip ""
    Category: [control](/cat/control)