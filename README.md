# Make My Debian Based Linux Workstation...
...somewhat comprehensible for my future self.

Having a consistent and comprehensible workstation is essential.
This document should help me understand, why I did things the way I did.


## TLDR
TODO: I am undecided yet, if I am going with `ansible` or `run_once_install-packages.sh`


## My Linux machine as of now: Ubuntu 20.04


### Standard GNOME Desktop
Provided by ubuntu.

And additional packages:
`gnome-shell-extentions-gpaste gpaste gnome-tweaks`

Not quite sure, if `gnome-shell-*` is needed since I switched over to terminator


#### Fonts
```
git clone --depth 1 https://github.com/ryanoasis/nerd-fonts
cd nerd-fonts
./install.sh DejaVuSansMono
```
Use desktop application `gnome-tweaks` in order to set `Fonts` to
`DejaVuSansMono Nerd Font Book`


### terminator -- multiple GNOME terminals in one window
Provided by ubuntu


### ZSH
Provided by ubuntu


#### Prezto -- configuration framework for zsh
https://github.com/sorin-ionescu/prezto

#### Powerlevel10k -- a theme for Zsh 
https://github.com/romkatv/powerlevel10k


## Install and work with modern and efficient tools
### chezmoi -- manage your personal configuration files
https://github.com/twpayne/chezmoi

#### Initialize your configfiles on a second machine
```
chezmoi init git@github.com/erolneuhauss/dotfiles.git
chezmoi appy
```
### bat -- cat(1) clone with wings
https://github.com/sharkdp/bat


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


### rg -- ripgrep (search tool like ack and grep)
https://github.com/BurntSushi/ripgrep


### thefuck -- corrects errors in previous console commands
https://github.com/nvbn/thefuck


## Fun tools
### cowsay -- higlight what's important in your scripts
Provided by Ubuntu


### fortune -- put up random quotes
Provided by Ubuntu

Try out: `fortune | cowsay | lolcat`


### lolcat -- concatenate files in rainbow colors
https://github.com/busyloop/lolcat
