---
title: "Tips for Iterm"
date: 2023-07-11T21:48:04+08:00
showToc: true
tocOpen: true
---


Here are multiple commands that I commonly use.

## Split window
---
`cmd + d` for vertical split

`cmd + shift + d` for horizontal split

when the window is split, use `cmd + [` or `cmd + ]` to switch between them.


## Broadcast input
---
Sometimes I need to control many console at the same time, such as there are multiple remote machine to control, 
and I don't want to something like tmux, I will use broadcast input.
This trick will make every pane listen to your keyboard stroke

{{< figure
    src="../broadcast-input.png"
    width="400"
>}}

## Alert on next mark 
---

When I have a long run job, I will use this function to send the alert when the job is done.
(this doesn't work on remote machine)

{{< figure
src="../alert-on-next-mark.png"
width="400"
>}}


## Copy Mode
---

I always use copy mode to copy a command in the history or in the current pane.

{{< figure
src="../copy-mode.png"
width="400"
>}}
