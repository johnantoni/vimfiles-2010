## Introduction

What you see is my own personal VIM configuration, with all manner of plugins, color formats and cool status messages.

Feel free to fork and copy it as you want, you can even drop me a line to suggest improvements.

Best,


## Install Config

    git clone [url] ~/.vim
    ln -nfs ~/.vim/vimrc ~/.vimrc
    ln -nfs ~/.vim/gvimrc ~/.gvimrc

## Install Command-T

    cd ~/.vim/ruby/command-t
    ruby extconf.rb
    make

Afterwhich you'll be able to use Command-T (aka Textmate Goto File) with \t

## Build VIM from Source

Either download from vim.org and install with Mercurial or download from my github vim mirror with:

    git clone git://github.com/johnantoni/vim.git
    cd vim/src

Now if you're in linux i'd recommend install vim with ruby support via 

    ./configure --with-features=huge --enable-rubyinterp

But if your on OSX i'd recommend installing MacVIM as it's got ruby support baked in (plus it's a major pain to compile vim with ruby support in osx)

    ./configure --with-features=huge

Whatever you decide, compile and install with

    make
    sudo make install

If however you want to re-configure later, run this to clean the SRC directory before re-building:

    make distclean

## MacVim, HomeBrew and PeepOpen

For OSX users i'd recommend installing (MacVIM)[http://code.google.com/p/macvim/] rather than using the Terminal client.
Along with that install [HomeBrew](http://mxcl.github.com/homebrew/), it's a really efficient package manager for OSX.

And if you want the GoTo file that TextMate has (and CommandT provides) install (PeepOpen)[http://peepcode.com/products/peepopen] from PeepCode, reallu awesome (and support already baked into this config)

## Keys

    \    leader key
    i    switch to insert mode
    esc  switch out of insert mode

With the CommandT plugin installed you can do a TextMate go-to file with \t
After which you can start typing the file your after and it'll zero in on it

## Global .gitignore

Included with this git repository is a pretty decent .gitignore file which works quite well as the basis of your global ignore file.

To install the packaged .gitignore file to your global git config, do:

    git config --global core.excludesfile ~/.vim/.gitignore

## NERDTree

Open with :NERDTree
Create new file pressing 'a'
Switch windows with CTRL+ww

## Rebuild Help Docs

:helptags ~/.vim/doc

