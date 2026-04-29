# tiny-hid-als (Arduino `.ino` edition)

This project provides firmware for a USB HID Ambient Light Sensor (ALS) using a Digispark ATtiny85-compatible board and a BH1750FVI I2C light sensor module.

The firmware entrypoint is now a standard Arduino sketch: `tiny_hid_als.ino`.

## Hardware

- ATtiny85 (Digispark-compatible board)
- BH1750/BH1750FVI light sensor module (I2C)

## Schematic

![Digispark connected to BH1750](https://github.com/3cky/tiny-hid-als/raw/main/doc/tiny-hid-als.png)

## OS support

USB HID sensors framework is supported out of the box since Linux 3.7 and Windows 8.

## Arduino IDE setup

1. Open `tiny_hid_als.ino` in the Arduino IDE.
2. Select an ATtiny85/Digispark board profile.
3. Ensure the core/toolchain you use supports:
   - V-USB (`usbdrv`)
   - AVR headers (`<util/delay.h>`)
4. Build and upload the sketch to your board.

> Note: Digispark boards usually require plugging in/resetting at upload time.

## Project layout

- `tiny_hid_als.ino` — main Arduino sketch.
- `include/HidSensorSpec.h` — HID Sensor Class usage definitions/macros.
- `lib/bh1750` — BH1750 light sensor driver.
- `lib/vusb` — V-USB stack used for HID over USB.

## License

This project is distributed under GPLv3. See `LICENSE` for details.
