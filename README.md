# Tone Generator with Arduino

This project demonstrates a simple tone generator using an Arduino. The code produces a 440 Hz tone on a speaker connected to pin 10, with a specified delay between tones.

## Components

- Arduino (Uno, Nano, or similar)
- Piezo buzzer or speaker
- Connecting wires
- Breadboard (optional, for connections)

## Code

```cpp
int i;

void setup() {
    for(i = 0; i < 3; i++) {
        tone(10, 440);    // Play a tone of 440 Hz on pin 10
        delay(2000);      // Wait for 2 seconds
        noTone(10);       // Stop the tone on pin 10
        delay(1000);      // Wait for 1 second
    }
}

void loop() {
    // Nothing to do here
}
```

## How It Works

1. Initialization: In the setup() function, a loop runs three times to generate a tone.
2. Tone Generation: The tone() function is used to play a 440 Hz tone on pin 10 for 2 seconds.
3. Delay: After each tone, the noTone() function stops the tone, and a 1-second delay is added before the next tone is played.

## Functions Used

- tone(pin, frequency): Generates a tone on the specified pin at the given frequency.
- noTone(pin): Stops the tone on the specified pin.
- delay(milliseconds): Pauses the program for the specified number of milliseconds.

## Setup

1. Connect a piezo buzzer or speaker to pin 10 of the Arduino.
2. Ensure that the component is properly connected and powered.
3. Upload the code to your Arduino.
4. Observe the buzzer or speaker as it plays a 440 Hz tone three times, with pauses between tones.

## Conclusion
- This simple tone generator project is a basic example of how to use the tone() function with an Arduino. It can be used as a starting point for more complex sound or music projects.