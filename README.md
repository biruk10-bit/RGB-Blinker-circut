# 🎨 RGB LED Color Cycle — Arduino

A simple Arduino sketch that cycles an RGB LED through six colors — Red, Green, Blue, White, Purple, and Pink — using PWM to control brightness on each color channel, then loops back to the start.

## ✨ Features

- Cycles through 6 distinct colors, holding each for 1 second
- Uses PWM (`analogWrite`) to control an RGB LED's red, green, and blue channels
- Colors are stored in a simple array, making it easy to add, remove, or reorder them
- Automatically resets back to the first color after completing a full cycle

## 🛠️ Hardware Requirements

- Arduino board (Uno, Nano, or similar)
- 1x Common Cathode RGB LED (or 3 separate LEDs: red, green, blue)
- 3x current-limiting resistors (~220Ω recommended)
- Breadboard and jumper wires

## 🔌 Wiring

| RGB LED Pin | Arduino Pin |
|-------------|-------------|
| Red         | Pin 3 (PWM) |
| Green       | Pin 5 (PWM) |
| Blue        | Pin 6 (PWM) |
| Cathode (–) | GND         |

> **Note:** If using a Common Anode RGB LED, connect the anode to 5V instead of GND, and invert the color values in code (`255 - value`).

## 🎨 Color Values Used

| Color   | RGB Value           |
|---------|----------------------|
| Red     | (255, 0, 0)         |
| Green   | (0, 255, 0)         |
| Blue    | (0, 0, 255)         |
| White   | (255, 255, 255)     |
| Purple  | (180, 0, 255)       |
| Pink    | (255, 20, 147)      |

## 🚀 Getting Started

1. Wire the RGB LED to the Arduino as shown above.
2. Open the sketch in the [Arduino IDE](https://www.arduino.cc/en/software).
3. Select your board and port under **Tools**.
4. Upload the sketch.
5. Watch the LED cycle through each color, one per second.

## 📄 Code Overview

- `setup()` — configures the red, green, and blue pins as outputs.
- `loop()` — iterates through the `colors` array, calling `setColor()` for each one and holding it for 1 second before moving to the next.
- `setColor()` — a helper function that writes PWM values to the red, green, and blue pins to produce the desired color.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
