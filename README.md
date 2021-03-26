# XKB config

### `setxkbmap` and `xkbcomp`

`xkbcomp $file $DISPLAY` to try compiling

`setxkbmap -print > $file` to print the XKB config with macros/directives expanded

### Updating

- keep custom files in `$XDG_HOME/dc/xkb`, with folder structure mirrored
- update in `$XDG_HOME` and cp to update in `/usr/share/X11/xkb`
- locales are in `/usr/share/X11/locale` and `/usr/share/kf5/locale`

### Keycode customizations

the only keycode that the pc104 keyboard lacks is `93`, which immediately preceeds `key <LSGT> = 94`. i can't seem to find the actual pc105 definition, which only seems to exist in `$XKB/symbols/pc` as symbols.
- pain in the ass, since XKB/X11 seem to inject `inet(evdev)` for media keys -- and SOO_MUCH_MORE_!!! -- ... but only after your symbols have been loaded.
- one option is to create additional rules (which would appear in KDE's handy list of woefully incomplete checkboxes), but probably doesn't work for `replace key` and/or `key <OMG> = 101` definitions.

### Resources & Config examples

- [DreymaR's big bag of tricks](https://github.com/DreymaR/BigBagKbdTrixXKB)
- [Yoda layout](Inspired by https://d2qmzng4l690lq.cloudfront.net/resizer/1500x1000/r/MD-2822_20140706105404_346413e18d672383.jpg)


