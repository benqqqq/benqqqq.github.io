---
title: "My Start with ChatGPT"
date: 2023-06-21T12:40:29+08:00
showToc: true
tocOpen: true
---

Lately, many new AI tools are popping up, all thanks to ChatGPT gaining popularity.
Like most people, I started my journey with ChatGPT.

{{< figure
src="../chatgpt-logo.png"
width="200"
>}}

## 1. Using ChatGPT to answer tech question

I've found that I can ask ChatGPT many questions,
especially about technical stuff.
It can quickly answer small things like **syntax issues** or even solve **tough debugging problems**. 
It's a lot faster than trying to find answers on blogs or on Stack Overflow.

ChatGPT is also good at answering **open-ended questions.**
If I'm wondering about what tech tools to use or how to compare them,
ChatGPT gives me a good starting point.

## 2. Finding great prompts

Once I began using ChatGPT,
I discovered numerous resources for useful prompts.
One of my favorite resources is this GitHub Page: [awesome-chat-gpt](https://github.com/f/awesome-chatgpt-prompts)

I also found some tools that let people share and design prompts:
1. [Superpower ChatGPT](https://chrome.google.com/webstore/detail/superpower-chatgpt/amhmeenmapldpjdedekalnfifgnpfnkc)
2. [ChatGPT 萬能工具箱](https://chrome.google.com/webstore/detail/chatgpt-%E8%90%AC%E8%83%BD%E5%B7%A5%E5%85%B7%E7%AE%B1/fmijcafgekkphdijpclfgnjhchmiokgp)
3. [AIPRM for ChatGPT](https://chrome.google.com/webstore/detail/aiprm-for-chatgpt/ojnbohmppadfgpejeebfnmnknjdlckgj)

## 3. Making prompts that fit my needs

Even with all the prompts out there,
sometimes I need something more specific.
For example, a prompt for "software engineer" might be good for writing Python code.
But I want a prompt that's an expert in using tailwindcss in React, which is a very specific thing.
In those cases, I use a "prompt creator prompt" with GPT-4 a lot. 
It helps make great prompts from just a simple sentence.

https://benqqqq.github.io/gpt-tools/prompt-list

I also use the plugin [ChatGPT 萬能工具箱](https://chrome.google.com/webstore/detail/chatgpt-%E8%90%AC%E8%83%BD%E5%B7%A5%E5%85%B7%E7%AE%B1/fmijcafgekkphdijpclfgnjhchmiokgp)
with bookmark in browser to let me quickly jump to many kind of my personal designed prompt
{{< figure
src="../prompt-bookmark.png"
width="200"
>}}


## 4. Creating my own tool 

After using ChatGPT for a while,
I came to understand that it's essentially an application utilizing Large Language Models (LLM). 
However, I realized that a chat interface isn't always the most efficient solution.
In some scenarios, conversations can become too complex or disorganized, 
making it difficult to arrive at the intended outcome.I wanted a tool that let me control the conversation better.
That's why I made this tool: https://github.com/benqqqq/gpt-tools
It uses the OpenAI API to make a conversation and lets me design my own prompts.


## 5. Solving more complex problem

Sometimes, one prompt isn't enough to answer the question.
This led me to consider implementing a series of conversations to achieve a specific objective.
For instance, I wanted ChatGPT to take my input and follow three steps, each with its own result.

I started searching for a tool that could do that and found langchain. 
Next, I wondered if anyone had made a user interface for langchain. They have! Here are a few:

1. [LangFlow](https://github.com/logspace-ai/langflow)
2. [SuperAgent](https://github.com/ladjs/superagent)
3. [Flowise](https://github.com/FlowiseAI/Flowise)


I'm still wondering whether these tools will fit my requirement, that is the next step

