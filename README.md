# Arduino LED Blinking Circuit

This project implements a simple circuit using an Arduino board and 4 LEDs with different colors. The goal is to turn the LEDs on and off in sequence with a fixed delay.

## Required Components

- Arduino board (UNO)
- 4 LEDs (different colors)
- 4 × 220 ohm resistors
- Jumper wires
- Breadboard

## Circuit Diagram

![Arduino LED Blinking Schematic](schematic.png)  
*(Please place the circuit schematic image in the same folder as this README file and name it `schematic.png`.)*

**Schematic Description:**  
The longer leg (anode) of each LED is connected to one of the Arduino digital pins (2, 3, 4, 5). The shorter leg (cathode) of each LED is connected to the Arduino GND pin through a 220 ohm resistor.

## Arduino Code
```cpp
/*
  Project Name: Arduino LED Blinking Circuit
  Description: Turn 4 LEDs on and off in sequence with a 1-second delay between each step.
  Date: 2026-05-12
  Author: Amirrezaakbari
*/

int ledPins[] = {2, 3, 4, 5}; // Arduino pins connected to the LEDs

void setup() {
  // Set LED pins as outputs
  for (int i = 0; i < 4; i++) {
pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  // Turn LEDs on and off in sequence
  for (int i = 0; i < 4; i++) {
digitalWrite(ledPins[i], HIGH); // Turn on current LED
delay(1000);                    // Wait for 1 second
digitalWrite(ledPins[i], LOW);  // Turn off current LED
// The delay between turning off one LED and turning on the next is zero.
  }
}
