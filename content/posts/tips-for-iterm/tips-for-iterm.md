---
title: "Tips for Iterm"
date: 2023-07-11T21:48:04+08:00
showToc: true
tocOpen: true
---


Here are multiple commands that I commonly use.

## Split window
---
- To split the iTerm window vertically, use the shortcut `cmd + d`. 
- To split the window horizontally, use `cmd + shift + d`.
- Once the window is split, you can switch between the panes using `cmd + [` or `cmd + ]`.
- Once the window is split, you can use `cmd + shift + enter` to maximize active pane.

## Broadcast input
---

Sometimes I need to control multiple consoles simultaneously,
such as when managing multiple remote machines,
I will use the broadcast input feature.
This makes every pane listen to my keyboard strokes.
(Tip: This is a handy alternative to using tools like tmux.)

{{< figure
    src="../broadcast-input.png"
    width="400"
>}}

## Alert on next mark 
---

To receive an alert when a long-running job is done, 
I will use the "**Alert on Next Mark**" feature in iTerm.
Please note that this function does not work on remote machines.

{{< figure
src="../alert-on-next-mark.png"
width="400"
>}}


## Copy Mode
---

To copy a command from the history or within the current pane,
I will use the copy mode in iTerm.

{{< figure
src="../copy-mode.png"
width="400"
>}}


