# Spanish (ANSI) on Linux

The layout is XKB. It works on Ubuntu and on other distributions that use XKB: Debian, Fedora, Arch, and the rest.

There are two ways to install it. The user install is enough for GNOME and for desktops that read `~/.config/xkb`. The system install is needed if you use X11 with `setxkbmap`, or if you want the layout on the login screen.

The name that appears is **Spanish (ANSI)**. The bar indicator is **ESA**.

AltGr is the right Alt key. Dead accents `` ` ``, `´`, `¨`, the macron `¯`, the caron `ˇ`, and the dead dots wait for the next letter. Space after a dead accent types the accent alone.

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

The `countryList` in `evdev.xml` registers the layout under **Spain** and the Spanish-speaking countries of the Americas (plus Brazil, Guyana, Suriname, and French Guiana). Open one of those countries, or **Spanish**, and choose **Spanish (ANSI)**.

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

To have it show up in the graphical picker as well, add the `<layout>` block from `linux/xkb/rules/evdev.xml` inside `<layoutList>` in `/usr/share/X11/xkb/rules/evdev.xml`. Do not replace that file: the one in the repository contains only this layout.

In `/usr/share/X11/xkb/rules/evdev.lst`, in the `! layout` section, add:

```
  esansi          Spanish (ANSI)
```

An update of the `xkb-data` package can rewrite the files in `/usr/share/X11/xkb`. The copy in `~/.config/xkb` stays.

## Check

With Spanish (ANSI) active: `¡` and `¿` sit unshifted to the right of `0`. Shift+1 types `|`. AltGr+5 types `€`. AltGr+C types `ç`. The backslash key types `<` and `>`.
