** Introduction

What you see is my own personal VIM configuration, with all manner of plugins, color formats and cool status messages.

Feel free to fork and copy it as you want, you can even drop me a line to suggest improvements.

Best,


** Install Config

    git clone [url] ~/.vim
    ln -nfs ~/.vim/vimrc ~/.vimrc
    ln -nfs ~/.vim/gvimrc ~/.gvimrc

** Build VIM from Source

Either download from vim.org and install with Mercurial or download from my github vim mirror with:

    git clone git://github.com/johnantoni/vim.git
    cd vim/src
    ./configure --with-features=huge --enable-rubyinterp
    make
    sudo make install

This will compile and install VIM with all features along with the Ruby interpreter.

If however you want to re-configure later, run this to clean the SRC directory before re-building:

    make distclean

