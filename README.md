.vim
====

Just run the following commands via terminal to get perfectly set up:

```console
$ cd ~/
$ git clone --recursive https://github.com/jessfraz/.vim.git .vim
$ git submodule update --init
$ ln -sf $HOME/.vim/vimrc $HOME/.vimrc

$ cd $HOME/.vim
$ cd bundle/coc.nvim
$ yarn install

## Neovim
Put the following in ~/.config/nvim/init.vim:
```
let runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath=&runtimepath
source ~/.vimrc
```

## Pathogen
The vim dot files make use of the excellent [Pathogen](https://github.com/tpope/vim-pathogen) runtime path manager to install plugins and runtime files into their own private directiories.

Currently using version 2.4 of Pathogen
