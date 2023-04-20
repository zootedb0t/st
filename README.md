## st - simple terminal
ST is a simple terminal emulator for X which [sucks-less](https://git.suckless.org/st/). The following patches have been incorporated in this build.

<details><summary>Click to view</summary>

- [st-alpha](https://st.suckless.org/patches/alpha/st-alpha-20220206-0.8.5.diff) - Allow `st` to have transparency while keeping text opaque.
- [st-anysize](https://st.suckless.org/patches/anysize/st-anysize-20220718-baa9357.diff) - Allows st to resize to any pixel size.
- [st-bold-is-not-bright](https://st.suckless.org/patches/bold-is-not-bright/st-bold-is-not-bright-20190127-3be4cf1.diff) - This patch makes bold text rendered simply as bold, leaving the color unaffected.
- [st-boxdraw](https://st.suckless.org/patches/boxdraw/st-boxdraw_v2-0.8.5.diff) - This patch adds options to render most of the lines/blocks characters without using the font so that they align perfectly regardless of font, size.
- [st-charoffsets](https://st.suckless.org/patches/charoffsets/st-charoffsets-20220311-0.8.5.diff) - This patch allow you to adjust the glyph position, so it doesn't get clipped short.
- [dont-cut-text]() - Allow us to resize terminal window without cutting text.
- [st-dynamic-cursor-color](https://st.suckless.org/patches/dynamic-cursor-color/st-dynamic-cursor-color-0.9.diff) - Swaps the colors of your cursor and the character you're currently on.
- [st-externalpipe](https://st.suckless.org/patches/externalpipe/st-externalpipe-0.8.4.diff) - Reading and writing `st's` screen through a pipe.
- [st-glyph-wide-support-boxdraw](https://st.suckless.org/patches/glyph_wide_support/st-glyph-wide-support-boxdraw-20220411-ef05519.diff) - This patch fixes wide glyphs truncation.
- [st-ligatures-boxdraw](https://st.suckless.org/patches/ligatures/0.9/st-ligatures-boxdraw-20221120-0.9.diff) - Add support for ligatures.
- [st-scrollback](https://st.suckless.org/patches/scrollback/) - Add `scrollback` support to terminal.
- [st-xresources-with-reload-signal](https://st.suckless.org/patches/xresources/) - Allow changing terminal colors,fonts etc. without `recompiling or restarting` `st` from `.xresource` file.

</details>

## Features

- Fonts, colors etc. can be configured from `.Xresource` file. No need to `restart or recompile st`.
- Texts don't cut while resizing terminal.
- Support transparency while keeping text opaque. This is controlled by `alpha` variable in `config.def.h`
- Support font ligatures.
- Select `url` from terminal window. Put `st-urlhandler` in your path variable. Use <kbd>alt+u</kbd> to open url and use <kbd>alt+y</kbd> to copy url.
- Dynamic-color cursor support make terminal appealing and easy to follow cursor.

## Requirements

In order to build st you need the Xlib header files. `dmenu` for `linkhandler` scripts.

## Installation

```
git clone https://github.com/zootedb0t/st.git
cd st
sudo make clean install
```

Edit `config.mk` to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```
sudo make clean install
```


## Running st
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
