# Maker Studio

A browser-based editor for the Ibtikar Maker Hexagon (ATmega32U4).

## Included
- Arduino sketch editor
- Open and save `.ino` files
- Web Serial device selection in supported Chrome browsers over HTTPS
- Quick insertion of common Arduino library includes
- Ibtikar Maker hardware references

## Confirmed board profile
Ibtikar's official advanced guide instructs users to select **Arduino Leonardo** in the Arduino IDE. The Maker uses the ATmega32U4, so Maker Studio uses the Leonardo profile as its starting point.

## Still being built
- **Verify:** requires an AVR compiler.
- **Upload:** requires a browser-compatible uploader that supports the Leonardo's native USB bootloader and its port re-enumeration behavior.

Selecting the board and detecting it over USB do not, by themselves, compile or upload a sketch.

## References
- https://www.ibtikar.io/project/maker/
- https://www.ibtikar.io/wp-content/uploads/2021/08/Maker_Advanced_EN.pdf
- https://docs.arduino.cc/hardware/leonardo
