# LS-TTL-Simulog-unofficial
A simple browser replica (self-contained HTML) of SIMULOG, the educational hardware logic trainer from LD Didactic GmbH (Leybold). This project lets you build and test logic circuits in the browser. It is fully self-contained and runs without any server or installation, and on any device.

# IMPORTANT: It is made for german-speaking audiences only. I do not plan to make any translations or region/language detection as of now.

## Features
NEW (07.07.2026): 
* reworked visuals
* now input-to-input connections and bridges work properly
* drag and drop from the inventory AND existing pieces on the board are visualized correctly
* experimental logic diagram generator
* board connection plan generator ("Steckbrettanleitung")

* grid board: 6x4 layout matching the original board
* wire connections: draw colored cables between ports (red or blue), so you can have a cable salad just like the real deal
* double-buffered simulation: resolves timing race conditions, essential for sequential logic (like ring registers or flip-flops)
* floating inputs: open inputs default to high (value 1), same as physical TTL gates
* short circuit check: warns you if you connect an output to another output (important)
* touchscreen support: drag and drop works on mobile, plus tap-to-place module positioning and larger click zones
  * sidebar can be toggled to save space on small screens
* state saving: autosaves to local storage and supports import/export via json files. (I will not work on backwards compatibility if I ever update the file.)
* signal view: optional mode to highlight high lines (glow) and low lines (dimmed)

## Included Modules

* adapter/clock: clock dividers (1:1, 50:1, 2:1, 60:1), manual buttons, reset input, and logic ground (value 0)
* input: 4 toggle switches with status leds
* output: 4 leds with active-low enable pin
* logic gates: 4x AND, 4x NAND, 4x OR, 4x NOR, and 4x Inverters
* multiplexer: 4-channel MUX with select pin
* full adder: carry in/out and sum output
* jk flipflops: 2 flip-flops with set/reset and clock pins
* shift register: 4-bit register with parallel load, serial input, clock, and active-low reset
* hex display: 7-segment display showing characters 0 to F from binary inputs

ALL modules have been visualized via SVG. If anyone can provide a better design, I would appreciate it. 

## Getting Started

Just download the repository and open `index.html` (file name may change) in your browser. No build steps or server setup needed.

```bash
git clone dorcelessquack/LS-TTL-Simulog-unofficial.git
```

## Disclaimer

This is an unofficial fan recreation for educational purposes. It is not affiliated with, sponsored by, or associated with LD Didactic GmbH or Leybold. No proprietary code, firmware, or copyright assets from the original manufacturer are used.

## License

See the LICENSE file for details.
