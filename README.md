# fzfX

**fzfX** multiplies the power of [fzf](https://github.com/junegunn/fzf) by providing zero-configuration battle-tested applications to common use cases of fzf. It delivers the power of finding, previewing, editing and managing any file in few key strokes. 

<!-- TOC GFM -->

* [Features](#features)
    * [Find files anywhere](#find-files-anywhere)
    * [Find anything](#find-anything)
    * [Dynamically find a string inside files](#dynamically-find-a-string-inside-files)
    * [Change directory](#change-directory)
    * [Manage processes](#manage-processes)
    * [Find files with special cases](#find-files-with-special-cases)
* [Setup](#setup)
* [Configure](#configure)

<!-- /TOC -->

## Features
- **default**: find any file
- **hidden**: include hidden files
- **full**: fulltext, files containing string
- **md**: markdown notes
- **pdf**: pdf, ps and eps files
- **pic**: pictures
- **av**: audio and video
- **cd**: change directory
- **ps**: manage processes

It is agnostic and does not require a specific terminal emulator, desktop environment or text editor. It will make use of improved utils that are becoming standard at Linux desktop environments, like **rg**, **fd**, **bat**, **rga**, **grc** and many others. But it will sensibly fallback to their classic UNIX counterparts like **grep**, **cat** and **ls** when they are not available.

### Find files anywhere
[![asciicast](https://asciinema.org/a/405579.svg)](https://asciinema.org/a/405579)

```sh
$ fzfx
```

### Find anything
[![asciicast](https://asciinema.org/a/405581.svg)](https://asciinema.org/a/405581)

```sh
fzfx hidden
```

By default hidden files, cache/vendor directories like `node_modules` *(see /usr/share/fzfx/ignore)* are ignored and `.gitignore` files inside directories are followed.

### Dynamically find a string inside files
[![asciicast](https://asciinema.org/a/405583.svg)](https://asciinema.org/a/405583)

```sh
$ fzfx full
```

*Note: Supports regular expressions.*

### Change directory
[![asciicast](https://asciinema.org/a/405594.svg)](https://asciinema.org/a/405594)
```sh
$ fzfx cd
```

To change dir with ENTER create an alias:
```sh
alias fcd='cd "$(fzfx cd)"'
```
*Note: Needed because a child shell can't act on its parent.*

### Manage processes 
[![asciicast](https://asciinema.org/a/405584.svg)](https://asciinema.org/a/405584)

```sh
$ fzfx ps
```

### Find files with special cases
```sh
# markdown notes
$ fzfx md

# pdf, ps and eps
fzfx pdf

# pictures
fzfx pic

# audio and videos
fzfx av
```

## Setup
Install through the [AUR](https://aur.archlinux.org/packages/fzfx-git)

Or install as user
```sh
$ ./setup install
```
## Configure
Edit `$XDG_CONFIG_HOME/fzfx/config`

- Set `root="$HOME"` to search all your files from anywhere.
- Set `editor` to override the editor used by fzfx.
- Set `ignoreFile` to override the default ignore file *(.gitignore style)*.
- Set `defaultPreview`, `pdfView`, `avView`, `picView` to whatever you prefer.

*Note: All configurations are optional.*
