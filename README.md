# How to Computer

The purpose of this repo is to prevent me having to remember all the steps I go thru when i start a new PC or project.

## Setting up a new Windows PC
1. install VSCode, Chrome, Ubuntu22 WSL (on MS Store)
### WSL Setup
1. Open Powershell and type `wsl --install Ubuntu22.04`

### setup zsh
Mostly taken from https://itsfoss.com/zsh-ubuntu/ with thanks

get zsh
```
sudo apt install zsh git fonts-font-awesome
```
start zsh and press option 0
```
zsh
```
get oh my zsh
```
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
get auto suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
and syntax highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

and open `zshrc`
```
vim ~/.zshrc
```
and replace the line `plugins=...`
```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

now setup the font

Here, the default theme will be named robbyrussell which needs to be changed with `powerlevel10k/powerlevel10k`

finally, add some aliases (thanks ChatGPT)

```
#!/bin/bash
alias s="source ~/.zshrc"
alias aliases="vim ~/.zsh_aliases"
alias zshrc="vim ~/.zshrc"

# Navigation Aliases
alias ..='cd ..'                 # Go up one directory
alias ...='cd ../..'             # Go up two directories
alias ....='cd ../../..'         # Go up three directories
alias ll='ls -alF'               # List all files in long format
alias la='ls -A'                 # List all files, including hidden files
alias l='ls -CF'                 # List files in columns

# Random stuff
alias du='du -h'                 # Human-readable disk usage
alias df='df -h'                 # Human-readable disk free
```

and you're done!

