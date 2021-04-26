# Make My Debian Based Linux Workstation Somewhat Comprehensible For Myself ;-)
Having a consistent and comprehensible workstation is essential.
This document should help me understand, why I did things the way I did.
So, this is for my future me.


## TLDR
TODO: I am undecided yet, if I am going with `ansible` or `run_once_install-packages.sh`


## My Linux machine as of now: Ubuntu 20.04


### Standard GNOME Desktop
Provided by ubuntu
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



### chezmoi -- manage your personal configuration files
https://github.com/twpayne/chezmoi

Clone your dotfile repository, `cd` into it and run `chezmoi apply`


## Install and work with modern and efficient tools
### exa -- a modern replacement for ls
https://github.com/ogham/exa


### bat -- cat(1) clone with wings
https://github.com/sharkdp/bat


### fzf -- fzf is a general-purpose command-line fuzzy finder.
https://github.com/junegunn/fzf


### neovim -- hyperextensible Vim-based text editor
https://neovim.io/

