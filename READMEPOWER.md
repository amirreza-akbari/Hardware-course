## Arduino Code
```cpp
//Author: Amirrezaakbari

// Author: Amirrezaakbari

const int buttonPin = 2;
const int ledPin = 13;

bool ledState = false;
int lastButtonState = LOW;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);

  digitalWrite(ledPin, ledState);
}

void loop() {
  int currentButtonState = digitalRead(buttonPin);

  if (currentButtonState == HIGH && lastButtonState == LOW) {
    delay(50);  // Debounce
    ledState = !ledState;
    digitalWrite(ledPin, ledState);
  }

  lastButtonState = currentButtonState;
}
