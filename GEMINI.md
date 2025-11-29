# ZMK Corne Keyboard Firmware

## Project Overview

This repository contains a ZMK firmware configuration for a Corne split keyboard. The configuration is based on the [Miryoku](https://github.com/manna-harbour/miryoku) layout, which is a comprehensive ergonomic layout for small keyboards.

- **Keyboard:** Corne Choc
- **Controller:** nice!nano v2
- **Firmware:** ZMK
- **Keymap:** Miryoku (42-key `corne` mapping)

## Building the Firmware

The firmware is built automatically using GitHub Actions. The build process is defined in `.github/workflows/build.yml` and the build matrix in `build.yaml`.

To build the firmware locally, you will need to set up a ZMK development environment. See the [ZMK documentation](https://zmk.dev/docs/development/setup) for instructions.

Once your environment is set up, you can build the firmware with the following command:

```
west build -b nice_nano_v2 -- -DSHIELD=corne_left
```

Replace `corne_left` with `corne_right` to build the firmware for the right half of the keyboard.

## Development Conventions

The keymap is defined in `config/corne.keymap`. This file includes the base Miryoku layout and can be customized to your liking. See the Miryoku documentation for more information on customization.

The ZMK configuration is in `config/corne.conf`. This file can be used to enable or disable features such as RGB underglow, OLED displays, and sleep.
