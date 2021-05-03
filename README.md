# Make My Debian Based Linux Workstation...
...somewhat comprehensible for my future self.

Having a consistent and comprehensible workstation is essential.
This document should help me to reproduce my working environment on another
machine.


## My Linux machine as of now: Ubuntu 20.04
Clone this repository https://github.com/erolneuhauss/workstation.git
You will need to run some scripts.

### ZSH
Install Zsh:
```console
sudo apt install -y zsh
```

Set Zsh as your default shell:
```console
chsh -s /bin/zsh
```

Launch Zsh:
```console
zsh

# Do not configure zsh yet! This is done in the 'Prezto' section. See below.
(q)  Quit and do nothing

# and delete .zshrc, if exists
rm -f ~/.zshrc || true
```

### Prezto -- configuration framework for zsh
https://github.com/erolneuhauss/prezto (forked from sorin-ionescu/prezto)

In `zsh` shell clone the repository into `.zprezto` like this:
```console
git clone --branch main --recursive https://github.com/erolneuhauss/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
```

Create symbolic links to zsh configuration by running `./symlink_zsh_runcoms.sh`.

### chezmoi -- manage your personal configuration files
https://github.com/twpayne/chezmoi

On any other Debian based Linux workstation I am able to recreate my working
environment and my prefered applications with a few simple `chezmoi` commands.

#### Install chezmoi
Run `./install_chezmoi.sh`

#### Initialize your configfiles on a second machine
```console
chezmoi init git@github.com/erolneuhauss/dotfiles.git
chezmoi appy
```

This should install packages defined in `run_once_install-packages.sh` and
configure some '.dotfiles' but most importantly neovim.
There might be additional things to
consider and configure manually at this moment.

This is WIP.

TODO: setup vagrant and recreate local environment in a virtual machine

### Standard GNOME Desktop
Provided by ubuntu.

And additional packages:
`gnome-shell-extentions-gpaste gpaste gnome-tweaks`


### Nerd Font DejaVuSansMono
Installed via `run_once_install-packages.sh` in my `dotfiles.git`

Use desktop application `gnome-tweaks` in order to set `Fonts` to
`DejaVuSansMono Nerd Font Book`


## Install and work with modern and efficient tools
With `chezmoi appy` following tools are going to be installed besides a hole
bunch of other tools not mentioned here.

### bat -- cat(1) clone with wings
https://github.com/sharkdp/bat


### BpyTOP -- resource monitor with game style theme start up
https://github.com/aristocratos/bpytop


### delta -- a viewer for git and diff output
https://github.com/dandavison/delta


### diff-so-fancy -- human readable diffs
https://github.com/so-fancy/diff-so-fancy


### exa -- a modern replacement for ls
https://github.com/ogham/exa


### fasd -- offers quick access to files and directories
https://github.com/sorin-ionescu/prezto/tree/master/modules/fasd


### fd -- simple, fast and user-friendly alternative to find
https://github.com/sharkdp/fd


### fzf -- a general-purpose command-line fuzzy finder
https://github.com/junegunn/fzf


### glances -- monitoring tool
https://github.com/nicolargo/glances


### k9s -- Kubernetes CLI To Manage Your Clusters In Style!
https://github.com/derailed/k9s


### ncdu -- NCurses Disk Usage
https://dev.yorhel.nl/ncdu


### neofetch -- a command-line system information
https://github.com/dylanaraps/neofetch


### neovim -- hyperextensible Vim-based text editor
https://neovim.io/

Plugins are installed via `dotfiles.git`


#### Powerlevel10k -- a theme for Zsh
https://github.com/romkatv/powerlevel10k


### ranger -- console file manager with VI key bindings
https://github.com/ranger/ranger


### rg -- ripgrep (search tool like ack and grep)
https://github.com/BurntSushi/ripgrep


### terminator -- multiple GNOME terminals in one window
Provided by ubuntu


### thefuck -- corrects errors in previous console commands
https://github.com/nvbn/thefuck


## Fun tools
### cowsay -- higlight what's important in your scripts
Provided by Ubuntu


### fortune -- put up random quotes
Provided by Ubuntu

Try out: `fortune | cowsay | lolcat`

My personal cheat sheet like forunes: https://github.com/erolneuhauss/fortunes


### lolcat -- concatenate files in rainbow colors
https://github.com/busyloop/lolcat


### pokemonsay -- Pokemon version of cowsay with CLI and API
https://github.com/possatti/pokemonsay


### xcowsay -- displays a cute cow mand message on your Linux Desktop
Provided by Ubuntu

