#bm-e-z
## Synopsis
zsh plugin to share the emacs bookmarks with zsh bookmark.

zsh bookmark is provied by [cd-bookmark](https://github.com/mollifier/cd-bookmark.git).

The original script is licensed under the [MIT License](http://mokemokechicken.mit-license.org/).

## CAUTION

*cd-bookmark can not use, because cd-bookmark file is initialized by bm-e-z.*

## How to install
  1. install cd-bookmark (see, https://github.com/mollifier/cd-bookmark.git)
  2. put bm-e-z file in your $fpath
  3. if you need, _bm-e-z file also put in $fpath
 
        $ ls .zsh/functions/
          bm-e-z _bm-e-z cd-bookmark/
 
  4. add this line to your .zshrc:

     autoload -Uz bm-e-z
	 
  5. if need, edit bm-e-z file to configure  both emacs bookmark file and cd-bookmark file path

  6. You can set alias to this function.

        $ alias bm='bm-e-z'

***

*default setting*

em='/Applications/Emacs24.app/Contents/MacOS/bin/emacsclient'

your bookmark files select

EMACS_BOOKMARK=~/.emacs.d/bookmarks

EMACS_BOOKMARK=~/.emacs.bmk

CDBOOKMARK=~/.cdbookmark

***

## Usage

+ ### add current directory to bookmark(Emacs)

        $ bm-e-z -a


+ ### update bookmark (load bookmark from Emacs)

        $ bm-e-z -u

+ ### cd 

        $ bm-e-z [TAB, select directory]

+ ### show list (update bookmark, at same time)

        $ bm-e-z -l

+ ### show help

        $ bm-e-z -h

+ ### if you want to edit bookmark,

        edit Emacs bookmark,

        do not edit cd-bookmark file(default file is ~/.cdbookmark)
