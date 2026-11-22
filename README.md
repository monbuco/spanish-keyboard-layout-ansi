# Spanish (ANSI)

A **Spanish keyboard layout for standard ANSI hardware** (104/105 keys, no ISO key left of Z). It remaps a US-style physical keyboard so Spanish and the other languages of South America are comfortable to type without buying an ISO keyboard from Spain or Latin America.

ANSI is the most widely sold keyboard form factor. Targeting it first opens a larger hardware market. Today this project is a **software layout**. Later it can become a **physical layer**: the same map printed on keycaps (legend-only change) for boards that ship ANSI.

System name: **Spanish (ANSI)**. Short indicator: **ESA**. Layout id: `esansi`.

| Platform | Files | Guide |
|---|---|---|
| Linux (XKB) | [`linux/xkb/`](linux/xkb/) | [`linux.md`](linux.md) |
| Windows | [`windows/esansi.klc`](windows/esansi.klc) | [`windows.md`](windows.md) |
| macOS | build with Ukelele | [`macos.md`](macos.md) |

## Goals

- Work on a **standard ANSI** keyboard and keep access to a wide range of commercial boards.
- Cover **Spanish** as the primary language, plus the other languages used in South America.
- Include **Portuguese** accents and **`ç` / `Ç`**.
- Expose **scientific and financial** notation on AltGr layers.
- Provide the **diacritics needed for pinyin and IAST** (macron, caron, dot above, dot below, and the usual acute / grave / diaeresis set).

Letter row stays QWERTY. Spanish essentials sit on keys that exist on ANSI:

- `ñ` `Ñ` where US has `;` `:`
- Dead `´` `¨` where US has `[` `{`
- `¡` `¿` unshifted to the right of `0`
- `<` `>` on the backslash key
- `ç` `Ç` on AltGr+C / AltGr+Shift+C
- `€` on AltGr+5

## Layers

### Normal

```
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬─────────┐
│ ` │ 1 │ 2 │ 3 │ 4 │ 5 │ 6 │ 7 │ 8 │ 9 │ 0 │ ¡ │ ¿ │ ◄─────  │
├───┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬───────┤
│ Tab │ q │ w │ e │ r │ t │ y │ u │ i │ o │ p │ ´ │ / │  <    │
├─────┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴───────┤
│ Caps │ a │ s │ d │ f │ g │ h │ j │ k │ l │ ñ │ ' │  Enter   │
├──────┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴──────────┤
│ Shift  │ z │ x │ c │ v │ b │ n │ m │ , │ . │ - │   Shift    │
└────────┴───┴───┴───┴───┴───┴───┴───┴───┴───┴───┴────────────┘
```

### Shift

```
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬─────────┐
│ ~ │ | │ @ │ # │ $ │ % │ ^ │ & │ ( │ ) │ = │ ! │ ? │ ◄─────  │
├───┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬───────┤
│ Tab │ Q │ W │ E │ R │ T │ Y │ U │ I │ O │ P │ ¨ │ \ │  >    │
├─────┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴───────┤
│ Caps │ A │ S │ D │ F │ G │ H │ J │ K │ L │ Ñ │ " │  Enter   │
├──────┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴──────────┤
│ Shift  │ Z │ X │ C │ V │ B │ N │ M │ ; │ : │ _ │   Shift    │
└────────┴───┴───┴───┴───┴───┴───┴───┴───┴───┴───┴────────────┘
```

### AltGr

```
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬─────────┐
│ ~ │ º │ ª │ · │ ¢ │ € │ ¬ │ © │ ′ │ ″ │ ° │ + │ * │ ◄─────  │
├───┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬───────┤
│ Tab │ ∞ │ ω │ ε │ ρ │ τ │ ← │ → │ ∫ │ œ │ π │ [ │ ] │  ≤    │
├─────┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴───────┤
│ Caps │ æ │ σ │ δ │ φ │ γ │ θ │ ↓ │ ∂ │ λ │ { │ } │  Enter   │
├──────┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴──────────┤
│ Shift  │ « │ » │ ç │ ∇ │ β │ ν │ μ │ ≈ │ ̣  │ ≠ │   Shift    │
└────────┴───┴───┴───┴───┴───┴───┴───┴───┴───┴───┴────────────┘
```

### AltGr + Shift

```
┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬─────────┐
│ ⁺ │ ¹ │ ² │ ³ │ ⁴ │ ⁵ │ ⁶ │ ⁷ │ ⁸ │ ⁹ │ ⁰ │ ± │ ⸮ │ ◄─────  │
├───┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬───────┤
│ Tab │ § │ ₩ │ Ω │ ® │ ™ │ ¥ │ ॐ │ ₹ │ Œ │ ∏ │ ` │ ^ │  ≥    │
├─────┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴───────┤
│ Caps │ Æ │ ∑ │ Δ │ ƒ │ Γ │ α │ ↑ │ ¶ │ ₺ │ ¯ │ ˇ │  Enter   │
├──────┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴──────────┤
│ Shift  │ “ │ ” │ Ç │ £ │ ₿ │ ₁ │ ₂ │ ₃ │ ˙ │ √ │   Shift    │
└────────┴───┴───┴───┴───┴───┴───┴───┴───┴───┴───┴────────────┘
```

## Usage notes

- **Dead keys:** `` ` ``, `´`, `¨`, plus AltGr macron `¯`, caron `ˇ`, and dots `̣` / `˙`. Press the accent, then the letter (or space for the accent alone). These cover Spanish, Portuguese, pinyin, and IAST-style transliteration.
- **AltGr** is Right Alt (Option on macOS).
- **Programming:** `[` `]` `{` `}` live on AltGr of `´` `/` `ñ` `'`. `<` `>` on `\`. `+` `*` on AltGr of `¡` `¿`.

## Quick install (Linux)

```bash
mkdir -p ~/.config/xkb/symbols ~/.config/xkb/rules
cp linux/xkb/symbols/esansi ~/.config/xkb/symbols/esansi
cp linux/xkb/rules/evdev.xml ~/.config/xkb/rules/evdev.xml
```

Log out and back in, then add **Spanish (ANSI)** in your input sources. Full steps: [`linux.md`](linux.md).

## Upstream

The long-term path for Ubuntu and other distros is a submission to [xkeyboard-config](https://gitlab.freedesktop.org/xkeyboard-config/xkeyboard-config). Windows and macOS keep their platform-native packages beside the XKB sources.
