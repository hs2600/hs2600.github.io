---
layout: kba 
title: Vim number increment shortcut
date:   2024-01-21 00:00:00 -0800
description: VIM shortcut to increase a number
author: horacio 
image:  '/images/photo-1.jpeg'
tags:   [vim, linux, kba]
tags_color: '#477690'
---

## Option 1

First insert `1.` at the start of the first line.

Go to the start of the second line and go into record mode with `qa`.

Press the following key sequence:

```
i                           # insert mode
<Ctrl-Y><Ctrl-Y><Ctrl-Y>    # copy the first few characters from the line above  
<ESC>                       # back to normal mode
0                           # go back to the start of the line
<Ctrl-A>                    # increment the number
j                           # down to the next line
q                           # stop recording
```

Now you can play back the recording with `@a` (the first time; for subsequent times, you can do `@@` to repeat the last-executed macro) and it will add a new incremented number to the start of each line.

## Option 2

Here's an easy way to increase multiple line numbers, without recording a macro:

Make a blockwise, visual selection on the first character of each list item:

```
<Ctrl-V>2j
```

Insert a `0.` at the beginning of these lines:

```
I0. <Esc>
```

Re-select the visual selection (which is now all of the 0s) with `gv` and increment them as a sequence `g<Ctrl-A>`:

```
gvg<Ctrl-A>
```

The entire sequence:

```
<Ctrl-V>2jI0.<Esc>gvg<Ctrl-A>
```

### Helpful vi commands

- `Ctrl-Y`  (Copy and paste character from above line)
- `Ctrl-A`    (Increment selected number by one)
- `Ctrl-V`    (Blockwise visual selection)
- `gv`        (Repeat last visual selection)
- `g<Ctrl-A>` (Increment multiple selected numbers by one)
- `qa`        (Start recording `q` on 'a' register)
- `@a`        (Play recording from 'a' register)
- `@@`        (Play last recording)

