## st - simple terminal

ST is a simple terminal emulator for X which sucks less. This fork is based on st 0.9 and is heavily patched. The following patches have been applied.

<ul>
<li>dont-cut-text</li>
<li>st-alpha</li>
<li>st-anysize</li>
<li>st-blinking-cursor</li>
<li>st-bold-is-not-bright</li>
<li>st-boxdraw</li>
<li>st-charoffsets</li>
<li>st-dynamic-cursor-color</li>
<li>st-glyph-wide-support-boxdraw</li>
<li>st-hidecursor</li>
<li>st-ligatures-boxdraw</li>
<li>st-newterm</li>
<li>st-scrollback</li>
<li>st-undercurl</li>
<li>st-xresources</li>
</ul>

All patches can be found in patch directory.

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

Configuration is done through modifying config.def.h file.
After modifying to remove config.h, and recompile using above command.

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
