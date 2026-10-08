# ZMK Config — Corne (nice!nano v2)

Personal ZMK firmware configuration for a Corne split keyboard.

## Hardware

| Part | Details |
|------|---------|
| Controller | [nice!nano v2](https://nicekeyboards.com/nice-nano/) (both halves) |
| Shield | Corne (42 keys) |
| Display | nice!view e-paper with nice_view_adapter |

## Keymap

Five layers:

| Layer | Trigger | Purpose |
|-------|---------|---------|
| `noted` | default | [Noted layout](https://neo-layout.org/Layouts/noted/) — German-optimized base layer with umlauts (ä, ö, ü, ß) |
| `qwerty` | toggle with `QWRTY` on the media layer (below BT0) | Standard QWERTY fallback; press `QWRTY` again to return to Noted |
| `symbol` | hold `Sym` (bottom outer key, either side) | Symbols and punctuation |
| `number` | `Sym` + outer thumb (Ctrl / AltGr position) | Numbers (0–9), F-keys (F1–F15), arrow keys |
| `media` | `Sym` + middle thumb (Space / Enter position) | Media controls, Bluetooth profiles, QWERTY toggle |

Legend: `▽` transparent (falls through to the layer below), `·` no-op.

### noted (default)

```
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┐
│ Tab  │  Z   │  Y   │  U   │  A   │  Q   │   │  P   │  B   │  M   │  L   │  J   │  ß   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│Shift │  C   │  S   │  I   │  E   │  O   │   │  D   │  T   │  N   │  R   │  H   │Shift │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│ Sym  │  V   │  X   │  Ü   │  Ä   │  Ö   │   │  W   │  G   │  ,   │  .   │  K   │ Sym  │
└──────┴──────┴──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┴──────┴──────┘
                     │ Ctrl │Space │ Alt  │   │ Bksp │Enter │AltGr │
                     └──────┴──────┴──────┘   └──────┴──────┴──────┘
```

### qwerty (toggled)

```
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┐
│  ▽   │  Q   │  W   │  E   │  R   │  T   │   │  Y   │  U   │  I   │  O   │  P   │  ▽   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ▽   │  A   │  S   │  D   │  F   │  G   │   │  H   │  J   │  K   │  L   │  ;   │  ▽   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ▽   │  Z   │  X   │  C   │  V   │  B   │   │  N   │  M   │  ,   │  .   │  /   │  ▽   │
└──────┴──────┴──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┴──────┴──────┘
                     │  ▽   │  ▽   │  ▽   │   │  ▽   │  ▽   │  ▽   │
                     └──────┴──────┴──────┘   └──────┴──────┴──────┘
```

### symbol

```
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┐
│  ·   │  !   │  _   │  [   │  ]   │  ^   │   │  !   │  <   │  >   │  =   │  &   │  @   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ·   │  \   │  /   │  {   │  }   │  *   │   │  ?   │  (   │  )   │  -   │  :   │  ·   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ·   │  #   │  $   │  |   │  ~   │  `   │   │  +   │  %   │  "   │  '   │  ;   │  ·   │
└──────┴──────┴──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┴──────┴──────┘
                     │ Num  │Media │  ·   │   │  ·   │Media │ Num  │
                     └──────┴──────┴──────┘   └──────┴──────┴──────┘
```

### number

```
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┐
│  ·   │ F11  │ F12  │ F13  │ F14  │ F15  │   │  7   │  8   │  9   │  ·   │  ·   │  ·   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ·   │  F6  │  F7  │  F8  │  F9  │ F10  │   │  4   │  5   │  6   │  ·   │  ↑   │  ·   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ·   │  F1  │  F2  │  F3  │  F4  │  F5  │   │  1   │  2   │  3   │  ←   │  ↓   │  →   │
└──────┴──────┴──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┴──────┴──────┘
                     │  ▽   │  ▽   │  ▽   │   │  ·   │  0   │  ·   │
                     └──────┴──────┴──────┘   └──────┴──────┴──────┘
```

### media

```
┌──────┬──────┬──────┬──────┬──────┬──────┐   ┌──────┬──────┬──────┬──────┬──────┬──────┐
│  ▽   │ Prev │ Play │ Stop │ Next │  ▽   │   │ BT0  │ BT1  │ BT2  │ BT3  │ BT4  │BTClr │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ▽   │  ▽   │ Vol- │ Mute │ Vol+ │  ▽   │   │QWRTY │  ▽   │  ▽   │  ▽   │  ▽   │  ▽   │
├──────┼──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┼──────┤
│  ▽   │  ▽   │  ▽   │  ▽   │  ▽   │  ▽   │   │  ▽   │  ▽   │  ▽   │  ▽   │  ▽   │  ▽   │
└──────┴──────┴──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┴──────┴──────┘
                     │  ▽   │  ▽   │  ▽   │   │  ▽   │  ▽   │  ▽   │
                     └──────┴──────┴──────┘   └──────┴──────┴──────┘
```

### Host layout and unicode

The keymap assumes the host OS keyboard layout is **US**. Umlauts and ß are sent as
unicode sequences via [zmk-unicode](https://github.com/urob/zmk-unicode), so the host
needs a matching unicode input method:

- **Linux** — IBus (`Ctrl+Shift+U`)
- **macOS** — add *Unicode Hex Input* under System Settings → Keyboard → Input Sources and select it

### Bluetooth

The media layer exposes five Bluetooth profiles (BT0–BT4) and a clear key. Selecting BT0 also
switches unicode input to Linux mode; BT1 switches to macOS mode.

## Dependencies

Managed via [west](https://docs.zephyrproject.org/latest/develop/west/index.html) (`config/west.yml`):

- [zmkfirmware/zmk](https://github.com/zmkfirmware/zmk)
- [urob/zmk-unicode](https://github.com/urob/zmk-unicode) — unicode key support
- [mctechnology17/zmk-nice-oled](https://github.com/mctechnology17/zmk-nice-oled) — custom OLED/e-paper widgets

## Building

Firmware is built automatically via GitHub Actions on every push. Download the artifacts (`left.uf2` / `right.uf2`) from the [Actions tab](../../actions) and flash each half by double-pressing the reset button to enter bootloader mode, then dragging the `.uf2` file onto the mounted drive.

To build locally, follow the [ZMK getting started guide](https://zmk.dev/docs/development/setup).

## License

[MIT](LICENSE)
