# vim-errormarker

Highlights and sets error markers for lines with compile errors

- Author: Michael Hofmann

## Introduction

Hooks the make quickfix command and converts all compiler errors into signs that are placed next to the line with the error.
Additionally, lines with errors are highlighted.
Hover with your mouse over such a line to get the error message in a tooltip (only gui), or press \cc. The error markers will be updated on every call to :make.

## Screenshots

Doxygen in action with a lot of errors: ![doxygen screenshot](https://mh21.github.io/vim-error-markers-doxygen.png)

## Installation

Use [pathogen.vim](https://github.com/tpope/vim-pathogen).

    cd ~/.vim/bundle
    git clone git://github.com/mh21/errormarker.vim

The help file will be automatically installed the next time VIM is launched.

## Configuration

To distinguish between warnings and errors for gcc messages, place sth. like this in your .vimrc:

    let &errorformat="%f:%l:%c: %t%*[^:]:%m,%f:%l: %t%*[^:]:%m," . &errorformat

If you use a different locale than English, this may be also needed:

    set makeprg=LANGUAGE=C\ make

## About

A changelog can be found at the end of [errormarker.txt](doc/errormarker.txt).

Get the latest version, submit pull requests, and file bug reports
on GitHub:

- https://github.com/mh21/errormarker.vim

If you like this plugin, please star and rate it on these sites:

- [GitHub](https://github.com/mh21/errormarker.vim)
- [Vim.org](http://www.vim.org/scripts/script.php?script_id=1861)
