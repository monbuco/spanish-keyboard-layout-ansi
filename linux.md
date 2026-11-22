# Spanish (ANSI) on Linux

The layout is XKB. It works on Ubuntu and on the other distributions that use XKB: Debian, Fedora, Arch, and the rest. It is not an Ubuntu-only file.

There are two ways to install it. The user install is enough for GNOME and for desktops that read `~/.config/xkb`. The system install is needed if you use X11 with `setxkbmap`, or if you want the layout on the login screen.

The name that appears is **Spanish (ANSI)**. The bar indicator stays ESA.

AltGr is the right Alt key. The accents `` ` ``, `´`, `¨`, the macron, the caron, and the two dead dots wait for the next letter. Space after a dead accent types the accent alone.

## User install

From the root of this repository:

```bash
mkdir -p ~/.config/xkb/symbols ~/.config/xkb/rules
cp linux/xkb/symbols/esansi ~/.config/xkb/symbols/esansi
cp linux/xkb/rules/evdev.xml ~/.config/xkb/rules/evdev.xml
```

If `~/.config/xkb/rules/evdev.xml` already exists, do not replace it. Open that file and add, inside `<layoutList>`, the `<layout>` block from `linux/xkb/rules/evdev.xml`.

Log out and log back in. The desktop reads that folder at startup.

### GNOME

Settings → Keyboard → Input Sources → Add.

The first screen lists languages. Open **Spanish**, **Portuguese**, **English**, **Dutch**, or **French** and choose **Spanish (ANSI)**.

You can also open a country from the list (Spain, Colombia, …): the layout is registered for those countries as well.

To switch keyboards: Super+Space, or the bar indicator.

### KDE Plasma

System Settings → Keyboard → Layouts → Add → Spanish (ANSI).

Plasma on Wayland uses the same `~/.config/xkb` folder. If Spanish (ANSI) does not appear in the list, use the system install.

## System install

Needed for `setxkbmap` and for the login screen. `setxkbmap` does not read `~/.config/xkb`.

```bash
sudo cp linux/xkb/symbols/esansi /usr/share/X11/xkb/symbols/esansi
setxkbmap esansi
```

To have it show up in the graphical picker as well, add the `<layout>` block from `linux/xkb/rules/evdev.xml` inside `<layoutList>` in `/usr/share/X11/xkb/rules/evdev.xml`. Do not replace that file: the one in the repository contains only Spanish (ANSI), and the system file contains every layout.

In `/usr/share/X11/xkb/rules/evdev.lst`, in the `! layout` section, add:

```
  esansi          Spanish (ANSI)
```

An update of the `xkb-data` package can rewrite the files in `/usr/share/X11/xkb`. The copy in `~/.config/xkb` stays.

## Check

With Spanish (ANSI) active: `¡` and `¿` sit unshifted to the right of `0`. Shift+1 types `|`. AltGr+5 types `€`. AltGr+C types `ç`. The backslash key types `<` and `>`.
