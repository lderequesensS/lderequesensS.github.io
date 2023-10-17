---
title: "My Love for Bash Zsh"
date: 2023-09-13T17:03:00-03:00
tags:
  - bash
draft: false
---
I have always liked running programs from my terminal, I like how it feels and also that I have to know what I'm doing (`rm -rf --no-preserve-root /`, I'm looking at you). So it was just the next step to learn about piping commands, functions, variables and more.

In the last few months I have been trying to automate, or just shrink, some of my most used commands, for example for git some of my aliases are:

```bash
alias gs='git status'
alias gdc='git diff --staged'
alias gpo='git push --set-upstream origin $(git rev-parse --abbrev-ref HEAD)'
```
And a lot more, I know they are easily breakable but since I'm the only one using them is not an issue.

A few days ago I had an idea for two fairly complex tasks:
1. I have a folder where I store recording of my interviews, I want to transcribe them and also because I have a horrible memory and I could forget something important. I want a script to tell me how many hours of recordings I have.
2. I have been using more and more `git commit --fixup=<commit hash>`, I found it really useful to have a git history more organized but since I need to get the commit hash I have to constantly run `git log`, copy the hash, write the command, paste the commit and finally check if I didn't mess it up. I want a script that tells me the last 10 commits and I could choose it with easy numbers.

It is possible that exists an easier way to do this tasks but since I didn't find it I am going to just code it.

## What did I learn?
I thought that `zsh` and `bash` were 1:1 on everything, but I had an issue where running `read` it is impossible inside `zsh` and I had to use `vared`, nothing terrible really, I just didn't encounter this in the past. 

Also, why does `read -p` write to std error the text that you pass to it?, this is from its man page:
```
-p prompt
Display prompt on standard error, without a trailing newline, before attempting to read any input.  The prompt is displayed only if input is coming from a terminal.
```

---
You can get my scripts here: [GitHub](https://github.com/Leonardo-de-Requesens/scripts)

