# Spanish (ANSI) on macOS

macOS does not use the Linux XKB files. Build a `.keylayout` (for example with [Ukelele](https://software.sil.org/ukelele/)) from the map in the [README](README.md), or use the file in `macos/` when it is added.

On this system AltGr is the **Option** key. Right Option does the same.

Dead accents `` ` ``, `´`, `¨`, Option tilde `~`, Option+Shift grave and circumflex `` ` `` / `^` (for Portuguese), the macron, the caron, and the dead dots wait for the next letter. Space after a dead accent types the accent alone.

## Create the layout with Ukelele

1. Install [Ukelele](https://software.sil.org/ukelele/).
2. File → New from current input source (start from a US or Spanish keyboard).
3. Remap the keys to the four layers in the [README](README.md): normal, Shift, Option (AltGr), Option+Shift.
4. Set the name to **Spanish (ANSI)** and the short code to **ESA**.
5. Save as `Spanish ANSI.keylayout`.

## User install

1. In Finder, Go → Go to Folder… and open:

```text
~/Library/Keyboard Layouts
```

If the folder does not exist, create it.

2. Copy the `.keylayout` file there.
3. Log out and log back in. macOS reads layouts at startup.

To make it available to every account on the Mac, copy the file to `/Library/Keyboard Layouts`. That folder asks for an administrator password.

## Turn it on

System Settings → Keyboard → Input Sources → Edit → +.

In the language column, scroll to **Other** and choose **Spanish (ANSI)**. If the search field in that window finds the name, typing ESA also works.

Turn on Show Input menu in menu bar. That menu switches layouts. The default shortcut is often Control+Space; if it clashes with another, change it in System Settings → Keyboard → Keyboard Shortcuts → Input Sources.

## Remove

In Input Sources, select Spanish (ANSI) and press −. Then delete the `.keylayout` from `~/Library/Keyboard Layouts` and log out.

## Check

With the layout active: `¿` sits unshifted to the right of `0`, and Shift on that key types `¡`. The next key is `?` / `!`. Shift+1 types `|`. Option+5 types `€`. Option+C types `ç`. The `\` key types `<` and `>`.
