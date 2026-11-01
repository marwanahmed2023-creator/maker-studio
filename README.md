# Maker Studio

A lightweight Chromebook-friendly sketch workspace for the Ibtikar Maker Hexagon (ATmega32U4).

Live site: https://marwanahmed2023-creator.github.io/maker-studio/

## What works in Maker Studio

- Edit Arduino sketches in the browser.
- Automatically save the current sketch in this browser's local storage.
- Create a new sketch and open or export `.ino` files.
- Insert common Arduino library include lines.
- Use the confirmed Ibtikar Maker board profile: Arduino Leonardo.

## Real compilation and USB upload

Maker Studio is a lightweight editor, not a standalone Arduino compiler or firmware uploader. To avoid fake Verify/Upload buttons, the **Open full Arduino IDE** action exports the current sketch and opens the Circuitera browser IDE:

https://circuitera.org/ide

Workflow:
1. Click **Open full Arduino IDE** in Maker Studio. It exports `MakerSketch.ino` and opens the IDE in a new tab.
2. Import `MakerSketch.ino` into the full IDE.
3. Select **Arduino Leonardo**.
4. Click Verify to compile.
5. Connect the Ibtikar Maker by USB and grant the browser serial permission.
6. Click Upload.

Circuitera documents a browser-based AVR-GCC compiler, Web Serial upload, Chromebook support, and Leonardo as a compile target. Upload compatibility with this specific Ibtikar Maker board has not yet been physically tested.

## Automated test

GitHub Actions compiles the repository's starter sketch using:

```sh
arduino-cli compile --fqbn arduino:avr:leonardo --warnings all sketch
```

This confirms the saved starter sketch compiles for the Leonardo profile. It does not compile the live editor contents or test a physical USB upload.

## References

- Ibtikar Maker: https://www.ibtikar.io/project/maker/
- Ibtikar advanced guide: https://www.ibtikar.io/wp-content/uploads/2021/08/Maker_Advanced_EN.pdf
- Circuitera IDE: https://circuitera.org/ide
- Circuitera IDE features and board support: https://circuitera.org/products/arduino-ide
- Arduino Leonardo: https://docs.arduino.cc/hardware/leonardo
