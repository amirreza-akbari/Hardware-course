# Arduino LED Blinking Circuit

This project implements a simple circuit using an Arduino board and 4 LEDs with different colors. The goal is to turn the LEDs on and off in sequence with a fixed delay.

## Arduino Code
```cpp
/*
  Project Name: Arduino LED Blinking Circuit
  Description: Turn 4 LEDs on and off in sequence with a 1-second delay between each step.
  Author: Amirrezaakbari
*/

int ledPins[] = {2, 3, 4, 5}; 

void setup() {

  for (int i = 0; i < 4; i++) {
pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {

  for (int i = 0; i < 4; i++) {
  digitalWrite(ledPins[i], HIGH); 
  delay(1000);                    
  digitalWrite(ledPins[i], LOW); 
  }
}
