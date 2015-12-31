# wmrc

A simple WM powered by wmutils, comprised of pure POSIX-compliant shell scripts.

## Appearance

![wmrc](img/wmrc.png)

## Installation

A simple, automated method of installation will be added later (Void template, CRUX port, Arch PKGBUILD), but not yet. Hold on.

Note that this expects that you run `startx` from a tty, not use a login manager (e.g. `gdm`, `sddm`, etc). 

First off,  you need to compile/install the following:

* wmutils/libwm
* wmutils/core
* My fork of wmutils/opt 
* killwa
* sxhkd
* dmenu (or some menu, I use interrobang)
* Any virtual terminal (if your terminal is not properly detected by `tln`, you will have to edit `tln`)

Highly recommended:

* lemonbar
* dash - insanely fast posix-compliant shell. symlink to /bin/sh for best performance in most scripts
* hsetroot - wallpaper
* compton - tearing protection and shadows and such
* dunst - notification daemon

If you don't already have them, copy `sxhkdrc.default` to `~/.config/sxhkd/sxhkdrc`, and copy `xinitrc.default` to `~/.xinitrc`.

Uncomment the features you would like in `.xinitrc`.

Copy `config.default` to `~/.config/wmrc/config`.

If you wish to use `pulsew`, then copy `colors.default` to `~/.colors`.

Navigate to `opt/` and run `make`. This is required for use of the mouse when focusing windows. If you do not want this, change `4` to `7` in `evhandle`.

Throw all the scripts somewhere in your PATH. Enjoy.

## TODO

* User guide, good documentation

# Known issues

* Please report them!

# Pull requests

If you want to help, please do!
