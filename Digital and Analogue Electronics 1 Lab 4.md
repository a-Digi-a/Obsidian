# Connecting the two circuits (count to 99)
- disconnected the 555 timer from one of the circuits
- connected the breadboard power rails together.
- connected pin 4 of the digit counter to pin 13 of the tens counter.
- connected pin 5 of the digit counter to pin 12 of the tens counter.
- This was discovered in the datasheet\

# Octal

0000 - 0
0001 - 1
0010 - 2
0011 - 3
0100 - 4
0101 - 5
0110 - 6
0111 - 7
1000 - 8

- Disconnect the wire from pin 7 of the counter to pin 6 of the decoder
- Connect pin 6 of the decoder to ground 
- Connect Q4 (pin 7) to the reset pin (pin 14) for both counters 
- connect Q4 (pin 7) of the digit counter to clock up (pin 5) of the tens counter

# Reset Button
- Connected a button to VCC. This button was wired to both reset pins of the counters. A 100k ohm pull down resistor was wired from both of these reset pins to ground.


| R   | S   | Q   | Q'  | P Q | P Q' |
| --- | --- | --- | --- | --- | ---- |
| 0   | 0   | 1   | 0   |     |      |
| 0   | 1   | 1   | 0   |     |      |
| 1   | 0   | 1   | 0   |     |      |
| 1   | 1   |     |     |     |      |
