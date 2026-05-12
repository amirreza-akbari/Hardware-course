# Arduino LED Blinking Circuit

This project implements a simple circuit using an Arduino board and 4 LEDs with different colors. The goal is to turn the LEDs on and off in sequence with a fixed delay.

## Arduino Code
```cpp
/*
  Project Name: Arduino LED Blinking Circuit
  Description: Turn 4 LEDs on and off in sequence with a 1-second delay between each step.
  Author: Amirrezaakbari
*/

const int ledPins[] = {10, 11, 12, 13};
const int numLeds = 4;
const int delayTime = 1000; 

void setup() {
  for (int i = 0; i < numLeds; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(ledPins[i], HIGH);
    delay(delayTime);
    digitalWrite(ledPins[i], LOW);
  }
}
