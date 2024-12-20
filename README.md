## Overview

This is a complete development configuration using git, vim, tmux, i3, and bash.


### Features

#### Shell aliases

- `gst` - git status
- `gad` - git add
- `gbr` - git branch
- `gcm` - git commit
- `gdi` - git diff
- `gdt` - git difftool
- `gco` - git checkout
- `glo` - pretty git log
- `gpv` - switch to previous git branch
- `to` - create tmux session named after current directory
- `to [name]` - create tmux session with name
- `ta [name]` - attach to tmux session, with tab completion
- `tl` - list tmux sessions
- `mkve [name]` - make a new virtualenv
- `wo [name]` - work on a virtualenv, with tab completion
- `py` - python
- `ipy` - ipython
- `fl` - flake8
- `rn` - ranger
- `xf` - extract various archive file types

#### Vim plugins

- [vundle](https://github.com/gmarik/vundle) - vim plugin manager
- [ctrlp](https://github.com/kien/ctrlp.vim) - quickly call files into buffers
- [vim-handlebars](https://github.com/nono/vim-handlebars) - handlebars template compatibility and syntax
- [vim-jinja2-syntax](https://github.com/Glench/Vim-Jinja2-Syntax) - jinja2 template compatibility and syntax
- [python-mode](https://github.com/klen/python-mode) - python niceties, wrapping, etc
- [syntastic](https://github.com/scrooloose/syntastic) - syntax and coding convention checker
- [tcomment_vim](https://github.com/tomtom/tcomment_vim) - easy comment/uncomment
- [vim-airline](https://github.com/bling/vim-airline) - pretty status bar
- [vim-bundle-mako](https://github.com/sophacles/vim-bundle-mako) - mako template compatibility and syntax
- [vim-colorschemes](https://github.com/flazz/vim-colorschemes) - lots of color options
- [vim-fugitive](https://github.com/tpope/vim-fugitive) - git branches and features
- [vim-golang](https://github.com/jnwhiteh/vim-golang) - Go compatibility and syntax
- [vim-less](https://github.com/groenewege/vim-less) - LESS compatibility and syntax
- [vim-surround](https://github.com/tpope/vim-surround) - surround text motion
- [vim-unimpaired](https://github.com/tpope/vim-unimpaired) - useful extra motions
- [matchit](https://github.com/tmhedberg/matchit) - use % to jump around html and other extras
- [python-matchit](https://github.com/voithos/vim-python-matchit) - use % to jump around python code
- [vim-sneak](https://github.com/justinmk/vim-sneak) - quickly jump to characters
- [emmet-vim](https://github.com/mattn/emmet-vim) - html expansion from selectors
- [jedi-vim](https://github.com/davidhalter/jedi-vim) - python autocomplete and function prototypes
- [neocomplete](https://github.com/Shougo/neocomplete.vim) - miscellaenous autocomplete

## Install

Clone the repository to a permanent home (configuration files will be symlinked):

    $ git clone https://github.com/gabrielstein/dotfiles.git
    $ cd dotfiles
    $ ./bootstrap.sh

### Options

`--git-name "[name]"` - Specify the full user.name for git configuration  
`--git-email [email] ` - Specify the full user.email for git configuration  
`--no-virtualenv` - Exclude virtualenvwrapper installation (using virtualenv-burrito)  
`--no-git` - Exclude git configuration  
`--no-i3` - Exclude i3 configuration  
`--no-vim` - Exclude vim configuration  
`--no-tmux` - Exclude tmux configuration  
`--no-ipython` - Exclude ipython configuration  

### Backups

By default, backups of your current dotfiles are created at `~/.filename.dotbackup`.

To delete the backups:

    $ ./bootstrap.sh --delete-backups

### Updating

    $ ./bootstrap.sh --update

## Software

### Fedora 25

    $ sudo yum|dnf install git tmux i3 ranger golang python python-devel htop python-setuptools curl

### Python tools

IPython is a fantastic python interactive shell, and flake8 lets vim show you where you're not adhering to python syntax or coding style.

    $ sudo easy_install pip
    $ sudo easy_install ipython
    $ sudo easy_install flake8 (Docs: http://flake8.pycqa.org/en/latest/)
