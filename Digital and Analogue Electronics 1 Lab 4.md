# Connecting the two circuits (count to 99)
- disconnected the 555 timer from one of the circuits
- connected the breadboard power rails together.
- connected pin 4 of the digit counter to pin 13 of the tens counter.
- connected pin 5 of the digit counter to pin 12 of the tens counter.
- This was discovered in the datasheet\


# Reset Button
- Connected a button to VCC. This button was wired to both reset pins of the counters. A 100k ohm pull down resistor was wired from both of these reset pins to ground.