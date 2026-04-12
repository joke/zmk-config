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
| `noted` | default | [Noted layout](https://noted.lol/) — German-optimized base layer with umlauts (ä, ö, ü, ß) |
| `qwerty` | — | Standard QWERTY fallback |
| `raise` | hold outer thumb | Symbols and punctuation |
| `number` | hold inner thumb | Numbers (0–9) and F-keys (F1–F15), arrow keys |
| `media` | both inner thumbs | Media controls and Bluetooth profile switching |

### Bluetooth

The media layer exposes five Bluetooth profiles (BT0–BT4) and a clear key. BT0 sets Linux unicode mode; BT1 sets macOS mode.

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
