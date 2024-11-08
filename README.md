# CCI-Libraries

This repository contains a small collection of libraries I've created for use with [Content Creator Integration (CCI)](https://www.curseforge.com/minecraft/mc-mods/content-creator-integration).

## Command Executor

This library tries to help with making more complicated commands. 

Background - The original inspiration for this was spawning many TNT on KojiroMC during one of his interactive streams. At first, the command spawned all TNT at once. Then delays were added so that it wasn't as devestating. This didn't follow him as he moved, however, so I began work on a new version. Once I finally learned how to achieve this, I wanted to simplify it and use it elsewhere.

### Variables and Definitions

By setting up a series of variables, you can create complicated commands with varying options. A few examples can be found in [chat.json](./default/chat.json).

#### General Variables

- `commandFeedback` - True/False to copy execute commands to chat. For debugging purposes.
- `executeAsSelf` - True/False. See: [executeAsSelf in the CCI docs for Command Outcome](https://content-creator-integration.readthedocs.io/en/latest/components/config/outcome/CommandOutcome/) 
- `array` - an array used when trying to get a random element from a string
- `randomElement` - the result when using GetRandomElementOfArray

#### Delayed Command Variables

- `dcommand_command` - the command to execute repeatedly, unless a `dcommand_array` is provided
- `dcommand_array` - an array of commands to choose from randomly to execute. Split commands with a | delimiter
- `dcommand_init` - the initial delay before the first command is executed
- `dcommand_delay` - the number of ticks between commands
- `dcommand_count` - the number of times to execute the command
- `dcommand_bossbar` - true/false to include a bossbar displaying the current progress. Include Bossbar.json variables if using this.

## Bossbar

This library helps manage bossbars. Simple enough, right?

### Variables and Definitions

- `bossbar_id` - a unique identifier for the bossbar
- `bossbar_color` - the color of the bossbar
- `bossbar_target` - the selector used for showing the bossbar (use `@a` for all players)
- `bossbar_title` - the text to show players
- `bossbar_total` - the number of pieces the bossbar is divided into
- `bossbar_value` - the current value of the bossbar