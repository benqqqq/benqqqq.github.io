---
title: "Tips for Vim"
date: 2023-05-25T14:01:06+08:00
---

I'm not the kind of person who uses a lot of Vim plugins and turns Vim into my primary programming IDE. Instead,
I utilize the "ideavim" plugin within PyCharm, which allows me to use Vim functionality within PyCharm's editor window. 
My ultimate goal is to perform all tasks using the keyboard, without relying on the mouse.

Around 1-2 years ago, I began transitioning to using Vim inside PyCharm. 
Initially, I found it challenging to type anything, but now I love how Vim helps me improve my productivity. 
Using Vim has become an enjoyable experience.

Here are some tips that I consider important or that required some effort to discover:

* Use [The Ultimate vimrc](https://github.com/amix/vimrc)


* **Relative line Number**  
  * Enable with `set relativenumber`
  * Pros: It allows for quick navigation to specific lines, such as using `20 k` to jump 20 lines up.
  * Cons: It loses the information of absolute line numbers, which may be inconvenient when you need to find a specific line number referenced in an error message.
  ![relativenumber.png](../relativenumber.png)

* **Scroll along with cursor**
  * Enable with `set scrolloff=20` to automatically scroll the text as the cursor moves with a 20-line offset.
  * This eliminates the need for manual scrolling.
 
  {{< youtube RX4ut4j5K5A >}}


To be continued ...
