# fzfX

**fzfX** is a wrapper to [fzf](https://github.com/junegunn/fzf) and code searching tools like rg, fd and rga that does specialized fuzzy searches.

- **hidden**: hidden files
- **md**: markdown files
- **full**: full text search among documents
- **pdf**: pdf, ps and eps files
- **media**: videos and audio files
- **cd**: browse directories and cd
- **ps**: search and manage processes

## Features
### cd
[![fcd-asciicast](https://asciinema.org/a/349907.svg)](https://asciinema.org/a/349907)

Create an alias like
```shell
alias fcd='cd $(fzfx cd)'
```
to change directory with ENTER.

### ps
[![fps-asciicast](https://asciinema.org/a/349904.svg)](https://asciinema.org/a/349904)

## Setup
Install through the [AUR](https://aur.archlinux.org/packages/fzfx-git)

Or install at Home
```shell
$ ./setup install
```
