# Spanish (ANSI) on Windows

Windows does not use the Linux XKB files. The layout is in [`windows/esansi.klc`](windows/esansi.klc). Compile it with Microsoft Keyboard Layout Creator and install the package that tool builds.

The keyboard is tied to **Spanish (Spain)**. In the list it appears as **Spanish (ANSI)**. You can use it while the rest of the system is in another language: Windows allows several keyboards and switches with Windows+Space.

AltGr is the right Alt key. Dead accents wait for the next letter. Space after a dead accent types the accent alone.

## Requirements

- Windows 10 or Windows 11, 64-bit.
- [Microsoft Keyboard Layout Creator 1.4](https://www.microsoft.com/en-us/download/details.aspx?id=102134).
- .NET Framework 3.5. If the installer asks for it: Settings → Apps → Optional features → More Windows features → .NET Framework 3.5.

## Install

1. Install Microsoft Keyboard Layout Creator.
2. Open it. File → Load Existing Keyboard… and choose `windows/esansi.klc`.
3. Project → Validate Layout. If there are no errors, continue.
4. Project → Build DLL and Setup Package. The program creates a folder with `setup.exe`.
5. Run `setup.exe` and finish the wizard.
6. Log out and log back in.

## Turn it on

Settings → Time & language → Language & region.

If **Spanish (Spain)** is not in the list, add it. On the three dots for that language: Language options → Keyboards → Add a keyboard → **Spanish (ANSI)**.

The keyboard switch is Windows+Space, or the taskbar indicator.

## Remove

Settings → Apps → Installed apps → Spanish (ANSI) → Uninstall.

Then, in the keyboards for Spanish (Spain), remove Spanish (ANSI) if it is still in the list.

## Check

With the layout active: `¿` sits unshifted to the right of `0`, and Shift on that key types `¡`. The next key is `?` / `!`. Shift+1 types `|`. AltGr+5 types `€`. AltGr+C types `ç`. The `\` key types `<` and `>`.
