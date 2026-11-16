
# Initial Arduino Tasks

- Changed both "delay" function parameters from 1000 to 500 (halved it)
- Changed the led variable from 13 to 11

# Light Dependent Resistor

Normal Resistance - 6.2k ohms
Covered value - 30k ohms
Torch value - 1k ohms

R = sqrt(Rmin * Rmax)
R = 5477.225575
we used 2.2k and 3.3k ohm resistors in series
![[Pasted image 20261116150106.png]]![[Pasted image 20261116150247.png]]

```C
// Analog Read and Serial Write

int ldrPin = A0;    // select the input pin A0 for the LDR input
int ldrValue = 0;   // variable to store the value coming from the LDR
int ledPin = 11;

void setup() {
  pinMode(ldrPin, INPUT);  // Set up the pin as an input pin
  Serial.begin(9600);      // Set up the serial output at 9600 baud
}

void loop() {
  // read the value from the LDR. This is a 10-bit ADC
  // so there will be 2^10 values (1024), values 0 to 1023.
  ldrValue = analogRead(ldrPin);    
  
  // send to the serial output the value
  Serial.print("LDR:");  // no 'ln' as I don't want a new line yet
  Serial.println(ldrValue); // print out the LDR value
  
  analogWrite(ledPin, 255-(ldrValue/4));
    
}
```

