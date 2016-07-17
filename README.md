# Dropsync
I'm too lazy to make a commit every single time I want to change my dotfiles
and need to manually go to all of my machines to pull that change.

This is when dropbox came in as a possible solution. Dropbox provide automated
syncing out of the box that doesn't need any supervision. It works on all of my
devices, including on linux.

Dropsync is a simple script that takes your dotfiles locally, add it to dropbox
then symlink it.

## Motivations
1. Laziness
2. Productivity
3. Need for customization

## Requirements
Sign up for and install dropbox
`https://www.dropbox.com/`

If you are on a linux box with no screen
`https://www.dropbox.com/install?os=lnx`

## Installation
```
curl -o dropsync http://git.io/vRqjH && chmod +x dropsync
```

## Configuration
Dropsync pulls `.dropsync` from your home directory which is just an yaml file
that lists all the files you want to sync. You can only sync files in your home
directory at this moment.

Example:
```
---
- .tmux.conf
- .vimrc
- .zsh_history
```
