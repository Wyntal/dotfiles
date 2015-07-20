## What are in the repo
    dotfile
    ├── astylerc
    ├── git
    |   └── gitconfig
    ├── sublime
    |   ├── monokai-custom
    |   ├── Preference.sublime-settings
    |   └── README.md
    ├── tmux
    │   └── tmux.conf
    ├── vim
    │   ├── vimrc
    │   ├── vimrc.bundles
    │   ├── vimrc.bundles.airline
    │   ├── vimrc.bundles.airline.fonts
    │   ├── vimrc.bundles.colorschemes
    │   ├── vimrc.bundles.default
    │   ├── vimrc.bundles.snippets
    │   ├── vimrc.bundles.syntax
    │   └── vimrc.bundles.ycm
    └── zsh
        └── zshrc

## Why is the file or directory here

- astylerc - the config for **astyle** which is a format tool for *C*, *C++*, *C#*, *Java*. Also can used in VIM
- git - all things about _Git_
    - gitconfig - the config for **git**
- sublime - all things about _Sublime Text 2_
    - monokai-custom - git submodule, Monokai-custom colorscheme
    - Preference.sublime-settings - the Preference file
    - README.md - the list of sublime packages I use
- tmux - all things about _tmux_
    - tmux.conf - tmux config
- vim - all things about _VIM_
    - vimrc - the config for **vim**
    - vimrc.bundles - setup Vundle, and load other plugins
    - vimrc.bundles.airline - vim plugin vim-airline
    - vimrc.bundles.airline.fonts - set vim-airline to use powerline-fonts
    - vimrc.bundles.colorschemes - colorshemes
    - vimrc.bundles.default - all bundles except vim-snippets and YouCompleteMe
    - vimrc.bundles.snippets - vim plugin vim-snippets.
    - vimrc.bundles.syntax - vim syntax for different file types
    - vimrc.bundles.ycm - vim plugin YouCompleteMe. because install this plugin is not easy, so make it a separate task.
- zsh - all things about *zsh*
    - zshrc - the config for **zsh**, firstly generated by **[oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)**, and some other config added by me

## Tasks & Requirement
Available tasks:

- [vim_rc](#task-vim_rc)
- [vim_bundles_colorschemes](#task-vim_bundles_colorschemes)
- [vim_bundles_airline](#task-vim_bundles_airline)
- [vim_bundles_airline_with_fonts](#task-vim_bundles_airline_with_fonts)
- [vim_bundles](#task-vim_bundles)
- [vim_bundles_snippets](#task-vim_bundles_snippets)
- [vim_bundles_syntax](#task-vim_bundles_syntax)
- [vim_bundles_ycm](#task-vim_bundles_ycm)
- [git_config](#task-git_config)
- [git_dmtool](#task-git_dmtool)
- [git_extras](#task-git_extras)
- [git_flow](#task-git_flow)
- [astylerc](#task-astylerc)
- [sublime](#task-sublime)
- [zsh_rc](#task-zsh_rc)
- [tmux](#task-tmux)

You can do a specific task by run

    ./install.sh <taskname1>[ <taskname2> <tasknameN> ...]

- ### Task `vim_rc`
    Requirements: `git`, `vim`

    This task will not install any bundles, if you want to use some bundles, do __[task vim_bundles](#task-vim_bundles)__.

    You can override the system vim with the new one installed by `homebrew`.(OS X only. This is optional, but recommended, because system vim can't use system clipbord via register `+`)

        brew install macvim --override-system-vim

    And then add the new vim __PATH__ into your `$PATH`.

    Additionally, if you have installed `neovim`, this task will link `vim/vimrc` to `~/.nvimrc`.

- ### Task `vim_bundles_colorschemes`
    Requirement: `git`, `vim`, [task vim_rc](#task-vim_rc)

    Install colorschemes for vim.

- ### Task `vim_bundles_airline`
    Requirement: `git`, `vim`, [task vim_rc](#task-vim_rc)

    Install vim-airline for vim, without using powerline-fonts

- ### Task `vim_bundles_airline_with_fonts`
    Requirement: `git`, `vim`, [task vim_rc](#task-vim_rc)

    Install vim-airline for vim, with using powerline-fonts

- ### Task `vim_bundles`
    Requirements: `git`, `vim`, [task vim_rc](#task-vim_rc)

    #### What vim bundles are included in vimrc

        Plugin 'gmarik/Vundle.vim'
        Plugin 'tomasr/molokai'
        Plugin 'altercation/vim-colors-solarized'
        Plugin 'godlygeek/tabular'
        Plugin 'plasticboy/vim-markdown'
        Plugin 'leafgarland/typescript-vim'
        Plugin 'kchmck/vim-coffee-script'
        Plugin 'groenewege/vim-less'
        Plugin 'smilekzs/vim-nfo'
        Plugin 'evanmiller/nginx-vim-syntax'
        Plugin 'tmux-plugins/vim-tmux'
        Plugin 'pangloss/vim-javascript'
        Plugin 'tmux-plugins/vim-tmux-focus-events'
        Plugin 'Yggdroot/indentLine'
        Plugin 'ntpeters/vim-better-whitespace'
        Plugin 'bling/vim-airline'
        Plugin 'Marslo/vim-coloresque'
        Plugin 'terryma/vim-smooth-scroll'
        Plugin 'Raimondi/delimitMate'
        Plugin 'vim-scripts/matchit.zip'
        Plugin 'mattn/emmet-vim'
        Plugin 'tpope/vim-surround'
        Plugin 'tpope/vim-repeat'
        Plugin 'airblade/vim-gitgutter'
        Plugin 'dyng/ctrlsf.vim'
        Plugin 'scrooloose/nerdtree'
        Plugin 'jistr/vim-nerdtree-tabs'
        Plugin 'scrooloose/nerdcommenter'
        Plugin 'terryma/vim-expand-region'
        Plugin 'terryma/vim-multiple-cursors'
        Plugin 'osyo-manga/vim-over'
        Plugin 'kien/ctrlp.vim'
        Plugin 'Lokaltog/vim-easymotion'
        Plugin 'SirVer/ultisnips'
        Plugin 'honza/vim-snippets'
        Plugin 'Valloric/YouCompleteMe'

- ### Task `vim_bundles_snippets`
    Requirement: `git`, `vim`, `wget`, `python`, [task vim_rc](#task-vim_rc)

    Install vim-snippets plugin for vim.

- ### Task `vim_bundles_syntax`
    Requirement: `git`, `vim`, [task vim_rc](#task-vim_rc)

    Install vim syntax for different file types

- ### Task `vim_bundles_ycm`
    Requirement: `git`, `vim`, `wget`, `python`, [task vim_rc](#task-vim_rc)

    Install YouCompleteMe plugin for vim.

- ### Task `git_config`
    Requirement: `git`

    __What others maybe you should install?__

    - Kaleidoscope( _OS X only_ ) - a sooooo excellent diff and merge tool
    - git-extras - some useful tools for git, install from <https://github.com/tj/git-extras>( _Linux, OS X_ )
    - git-flow - a post about git-flow: [a-successful-git-branching-model](http://nvie.com/posts/a-successful-git-branching-model/), install from <https://github.com/nvie/gitflow>( _Linux, OS X_ ) or

            # OS X only
            brew install git-flow

- ### Task `git_dmtool`
    Requirement: `MAC`, `git`, `Kaleidoscope`(`ksdiff`)

    Config git's difftool and mergetool to Kaleidoscope.

- ### Task `git_extras`
    Requirement: `git`

    Install `git-extras` plugin for git.

- ### Task `git_flow`
    Requirement: `git`

    Install `git-flow` plugin for git.

- ### Task `astylerc`
    Requirement: `astyle`. If you have installed `astyle` and press `Q` in vim, astyle will be used to format the *C*, *C++*, *C#*, *Java* file.

    __What others maybe you should install?__

    astyle

        # OS X only
        brew install astyle

- ### Task `sublime`
    Requirement: `git`, `Sublime Text 2`

    **bakup your preference file first!**

    If you use `Sublime Text 2`, this task will add user Preference for it, and also add a [`Monokai-custom`](https://github.com/Treri/sublime-monokai-custom) colorscheme which supports Markdown file highlight.

    After installing the preference, maybe you want to reset `font_face` and `font_size` to what you prefer in `Preference.sublime-settings`. Also you can see what sublime packages I used in [SublimePackages](sublime/README.md).

    If you use `VIM Mode` in Sublime Text 2 on OS X 10.8+, when you hold `h`, `l`, `j`, `k`, the cursor will not move `left` `right` `down` `up` continually like real VIM, the solution is below.

    > Mac OS X Lion introduced a new, iOS-like context menu when you press and hold a key
    > that enables you to choose a character from a menu of options. If you are on Lion
    > try it by pressing and holding down 'e' in any app that uses the default NSTextField
    > for input.

    > It's a nice feature and continues the blending of Mac OS X and iOS features. However,
    > it's a nightmare to deal with in Sublime Text 2 if you're running Vintage (Vim) mode,
    > as it means you cannot press and hold h/j/k/l to move through your file. You have
    > to repeatedly press the keys to navigate.

    > You can disable this feature for just Sublime Text 2 by issuing the following command
    > in your terminal:

    >       defaults write com.sublimetext.2 ApplePressAndHoldEnabled -bool false

    > Alternately, if you want this feature disabled globally, you can enter this:

    >       defaults write -g ApplePressAndHoldEnabled -bool false

    > In either case you'll need to restart your computer for the change to take place.

    > Happy coding!

- ### Task `zsh_rc`
    Requirements: `git`, `zsh`

    If you have your own aliases, put them in `~/.zshrc.alias`, zsh will load them automatically.

    __What zsh plugins are used default?__

    - colored-man
    - git
    - git-extras
    - git-flow
    - sublime
    - sudo
    - tmux (when tmux is installed)
    - z
    - zsh-syntax-highlighting
    - brew (OS X only)
    - osx (OS X only)

    So, maybe you should install some of them to make full use of zsh.

- ### Task `tmux`
    Requirements: `git`, `tmux`

    tmux plugins
    - tmux-plugins/tpm
    - tmux-plugins/tmux-sensible
    - tmux-plugins/tmux-pain-control
    - tmux-plugins/tmux-resurrect
    - tmux-plugins/tmux-sidebar
    - tmux-plugins/tmux-copycat
    - tmux-plugins/tmux-yank

## LICENSE

The MIT License (MIT)

Copyright (c) 2013-2015 Treri treri.liu@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
