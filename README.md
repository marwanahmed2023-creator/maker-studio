# Maker Studio

A browser-based editor prototype for the Ibtikar Maker (ATmega32U4).

## Included
- Arduino sketch editor
- Open and save `.ino` files
- Web Serial USB connection test in supported Chrome browsers over HTTPS
- Quick insertion of common Arduino library includes
- Ibtikar Maker hardware references

## Not yet a complete flashing IDE
The Verify action needs a hosted Arduino CLI / AVR-GCC compiler service. Upload needs a bootloader-compatible uploader and confirmation of the Maker's exact board profile and bootloader settings. A successful USB serial connection does not mean code has been compiled or uploaded.

The Ibtikar documentation confirms the ATmega32U4 and Arduino compatibility, but does not by itself confirm the exact bootloader profile.

## References
- https://www.ibtikar.io/project/maker/
- https://www.ibtikar.io/wp-content/uploads/2021/08/Maker_Advanced_EN.pdf
