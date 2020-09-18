.vim
====

Just run the following commands via terminal to get perfectly set up:

```console
$ cd ~/
$ git clone --recursive https://github.com/breezykermo/.vim.git .vim
$ git submodule update --init
$ cp $HOME/.vim/vimrc $HOME/.vimrc

## extra installs
$ cd $HOME/.vim
$ cd bundle/coc.nvim && yarn # NPM won't work, it seems 
$ python3 -m pip install black

## Neovim
Put the following in ~/.config/nvim/init.vim:
```
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath=&runtimepath
source ~/.vimrc
```

## Pathogen
The vim dot files make use of the excellent [Pathogen](https://github.com/tpope/vim-pathogen) runtime path manager to install plugins and runtime files into their own private directiories.

Currently using version 2.4 of Pathogen
