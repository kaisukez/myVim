# Welcome to My Vim 
This is where I store my backup .vimrc file and plugin. So that when I install new linux or use another computer, I can synchronize my vim setting quickly.

I don't save plugin files, but I save the link to download plugin to Makefile. So that I can choose which plugin to install or install all of them.

## How to copy my vim
1. Clone my repository.
2. Move _plugs_ folder to where you want and move _autoload_ folder to ~/.vim.
3. Move _.vimrc_ to your home directory (backup if you want).
4. Choose plugin you want to use by __make__ command in _plugs_ folder.
5. Edit _.vimrc_.
6. Learn more about vim!

#### 1. Clone my repository
```
$ git clone git@github.com:kaisukez/myVim.git
```
#### 2. Move _plugs_ folder to where you want and move _autoload_ folder to ~/.vim
For example I move _plugs_ folder to ~/.vim because I want keep these files at the same place.
```
$ cd myVim
$ mv .vim/plugs ~/.vim
$ mv .vim/autoload ~/.vim
```
#### 3. Move _.vimrc_ to your home directory 
In my example I backup old _.vimrc_ to _.vimrc.bak_ then replace it with new _.vimrc_.
```
$ mv ~/.vimrc ~/.vimrc.bak
$ mv .vimrc ~/.vimrc
```

#### 4. Choose plugin you want to use
For example I want to install all plugin so that I use command __make all__.
```
$ cd ~/.vim/plugs
$ make all
```
But if you want to install specific plugin you can type __make__ following by plugin name such as I want to install _easymotion_ so I type...
```
$ make easymotion
```
And if you want to know which plugin you can install, you can use __cat__ or __less__ command to all plugin that I use.
```
$ cat Makefile
$ ALLPLUGINS = easymotion ctrlp autoformat airline airline-theme nerdtree ctrlspace undotree tagbar
```
#### 5. Edit _.vimrc_
Now you have to edit your _.vimrc_ file in order to make this vim to exactly suit to you. For example my _plugs_ directory is ~/.vim/plugs and my _ctags_ file is in ~/.vim/plugs/tagbar/ctags-5.8. So I change the _plugs_ path and _ctags_ path in _.vimrc_. If your _plugs_ directory is different, you can change it to where your _plugs_ directory is.
```vim
call plug#begin('~/.vim/plugs')
let g:tagbar_ctags_bin='~/.vim/plugs/tagbar/ctags-5.8/ctags'
```

#### 6. Learn more about vim!
Now you have set everything up. Next step is to learn vim. Sometimes you will find that this tutorial is too hard or you don't understand some of them, don't worry, you can search google to find the answer. If you want to learn about vim, you have to research alot, read everything, try every shortcut keys and try some plugins you want, customize your _.vimrc_. When you have learned some basics of vim, you will enjoy using vim and love vim like me.
