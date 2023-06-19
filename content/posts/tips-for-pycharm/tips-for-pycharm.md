---
title: "Tips for PyCharm"
date: 2023-05-24T14:26:27+08:00
draft: false
tags: ['IDE', 'PyCharm']
showToc: true
tocOpen: true
---

I'm a fan of speeding up everything when typing, and the IDE is one of the applications I use most frequently. 
Here are some tips to help me code faster:


## keymap
---
The keymap may differ for each individual, so your shortcuts may be different from mine. 
You can use the keymap settings to find the corresponding action by keystroke or name:
   1. Use `cmd + ,` to open the settings. 
   2. Use `cmd + f` to search for "keymap".
   ![keymap.png](../keymap.png)


## Open action
---
find any actions by its name
  * Use `cmd + shift + a`

   ![open-action.png](../open-action.png)

## Select (all) occurrences
---
This is useful when you want to change a variable name.

  * Use `ctrl + g` to find the next occurrence.
  * Use `ctrl + cmd + g` to find all occurrences.

  {{< youtube n85xm6ddLfI >}}


## Duplicate cursor
---
This allows you to have multiple cursors for editing.
  * Hold `opt` and `click` with the mouse, or use the `up or down arrow` while holding `opt`.

  {{< youtube 9HZbJnr5sKk >}} 


## Open in opposite group
---
This feature is useful when you have a split window in your IDE
and want to open the same file in the other panel. 
It comes in handy when you are working with a long file 
that requires editing while simultaneously referring to another position within the same file.

![open-in-opposite-group.png](../open-in-opposite-group.png)
![open-in-opposite-group-2.png](../open-in-opposite-group-2.png)


## Code completion shortcut
---
PyCharm has a default feature that enables code completion as you type in the editor. However, using a shortcut to manually trigger code completion can make you faster. Additionally, the default behavior requires you to type at least one character to trigger code completion, which can be problematic when you don't know what to type initially. In such cases, the default behavior doesn't work well for you.

Moreover, PyCharm provides many useful options to customize the "code completion" feature in the settings. I recommend customizing it based on your specific needs.

![code-completion-keymap.png](../code-completion-keymap.png)
![code-completion-demo.png](../code-completion-demo.png)
---

To be continued ...

