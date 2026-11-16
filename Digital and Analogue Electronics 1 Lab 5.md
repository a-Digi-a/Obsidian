
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
  
  int lightValue = 255-(ldrValue/4);

  Serial.print("Light Value:");  // no 'ln' as I don't want a new line yet
  Serial.println(lightValue); // print out the LDR value

  analogWrite(ledPin, lightValue);
    
}
```


```C
// Analog Read and Serial Write

int ldrPin = A0;    // select the input pin A0 for the LDR input
int ldrValue = 0;   // variable to store the value coming from the LDR
int ledPin = 11;
int invledPin = 12;

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
  
  int lightValue = 255-(ldrValue/4);
  lightValue = map(lightValue, 150, 220, 0, 255);
  Serial.print("Light Value:");  // no 'ln' as I don't want a new line yet
  Serial.println(lightValue); // print out the LDR value

  int invlightValue = ldrValue/4;
  invlightValue = map(invlightValue, 40, 100, 0, 255);
  Serial.print("Inverted Light Value:");  // no 'ln' as I don't want a new line yet
  Serial.println(invlightValue); // print out the LDR value

  analogWrite(ledPin, lightValue);
  analogWrite(invledPin, invlightValue);
    
}
```

```C
// The 7-Segment Display Counter
// The Counting Programme - Counts 0-9

void setup()  { 
// need to set up 7 pins for our 7-seg display - all as outputs
for(int i=2; i<=8; i++){  // pins 2 to 8 (i.e. 7 pins)
pinMode(i, OUTPUT); 
  }
} 

// This displays the number 0-9 by calling the displaySegment() function // and telling it which segments to light for the number 0..9. This 
// is not the most efficient way to do this but it is the easiest to
// understand. Just use this code.
void display(int x){
switch(x){  // x is the number to display 0-9
// e.g., for 0 light all segments except the middle one 
// which is segment g in Figure 9 above 
case 0: displaySegment(1,1,1,1,1,1,0);
break;
case 1: displaySegment(0,1,1,0,0,0,0);
break;
case 2: displaySegment(1,1,0,1,1,0,1);
break;
case 3: displaySegment(1,1,1,1,0,0,1);
break;
case 4: displaySegment(0,1,1,0,0,1,1);
break;
case 5: displaySegment(1,0,1,1,0,1,1);
break;
case 6: displaySegment(0,0,1,1,1,1,1);
break;
case 7: displaySegment(1,1,1,0,0,0,0);
break;
case 8: displaySegment(1,1,1,1,1,1,1);
break;
case 9: displaySegment(1,1,1,1,0,1,1);
break;
   }
} 

// This lights up the segments a-g which have been wired 2-8
void displaySegment(int a, int b, int c, int d, int e, int f, int g){
digitalWrite(2,a); // see Figure 9 to see a-g
digitalWrite(3,b);
digitalWrite(4,c);
digitalWrite(5,d);
digitalWrite(6,e);
digitalWrite(7,f);
digitalWrite(8,g);
}

// The loop() function will be called over-and-over, forever!
void loop()  { 
// count from 0 to 9 each time the loop() function is called
for(int i=0; i<=9; i++){
display(i);  // display 0, then 1, then 2... then 9.
delay(1000); // wait 1 second between each count
  }
}
```

```C
// The 7-Segment Display Counter
// The Counting Programme - Counts 0-9

int ldrPin = A0;
int ldrValue = 0;

void setup()  { 
// need to set up 7 pins for our 7-seg display - all as outputs
for(int i=2; i<=8; i++){  // pins 2 to 8 (i.e. 7 pins)
pinMode(i, OUTPUT); 
  }
pinMode(ldrPin, INPUT);
Serial.begin(9600);
} 

// This displays the number 0-9 by calling the displaySegment() function // and telling it which segments to light for the number 0..9. This 
// is not the most efficient way to do this but it is the easiest to
// understand. Just use this code.
void display(int x){
switch(x){  // x is the number to display 0-9
// e.g., for 0 light all segments except the middle one 
// which is segment g in Figure 9 above 
case 0: displaySegment(1,1,1,1,1,1,0);
break;
case 1: displaySegment(0,1,1,0,0,0,0);
break;
case 2: displaySegment(1,1,0,1,1,0,1);
break;
case 3: displaySegment(1,1,1,1,0,0,1);
break;
case 4: displaySegment(0,1,1,0,0,1,1);
break;
case 5: displaySegment(1,0,1,1,0,1,1);
break;
case 6: displaySegment(0,0,1,1,1,1,1);
break;
case 7: displaySegment(1,1,1,0,0,0,0);
break;
case 8: displaySegment(1,1,1,1,1,1,1);
break;
case 9: displaySegment(1,1,1,1,0,1,1);
break;
   }
} 

// This lights up the segments a-g which have been wired 2-8
void displaySegment(int a, int b, int c, int d, int e, int f, int g){
digitalWrite(2,a); // see Figure 9 to see a-g
digitalWrite(3,b);
digitalWrite(4,c);
digitalWrite(5,d);
digitalWrite(6,e);
digitalWrite(7,f);
digitalWrite(8,g);
}

// The loop() function will be called over-and-over, forever!
void loop()  { 
ldrValue = analogRead(ldrPin);
ldrValue = map(ldrValue, 0, 800, 0, 9); // Map to 800 as that was around the highest we got the LDR to go
display(ldrValue);  // display 0, then 1, then 2... then 9.
}
```

```C
// The 7-Segment Display Counter
// The Counting Programme - Counts 0-9

int ldrPin = A0;
int ldrValue = 0;

void setup()  { 
// need to set up 7 pins for our 7-seg display - all as outputs
for(int i=2; i<=8; i++){  // pins 2 to 8 (i.e. 7 pins)
pinMode(i, OUTPUT); 
  }
pinMode(ldrPin, INPUT);
Serial.begin(9600);
} 

// This displays the number 0-9 by calling the displaySegment() function // and telling it which segments to light for the number 0..9. This 
// is not the most efficient way to do this but it is the easiest to
// understand. Just use this code.
void display(int x){
switch(x){  // x is the number to display 0-9
// e.g., for 0 light all segments except the middle one 
// which is segment g in Figure 9 above 
case 0: displaySegment(1,1,1,1,1,1,0);
break;
case 1: displaySegment(0,1,1,0,0,0,0);
break;
case 2: displaySegment(1,1,0,1,1,0,1);
break;
case 3: displaySegment(1,1,1,1,0,0,1);
break;
case 4: displaySegment(0,1,1,0,0,1,1);
break;
case 5: displaySegment(1,0,1,1,0,1,1);
break;
case 6: displaySegment(0,0,1,1,1,1,1);
break;
case 7: displaySegment(1,1,1,0,0,0,0);
break;
case 8: displaySegment(1,1,1,1,1,1,1);
break;
case 9: displaySegment(1,1,1,1,0,1,1);
break;
   }
} 

// This lights up the segments a-g which have been wired 2-8
void displaySegment(int a, int b, int c, int d, int e, int f, int g){
digitalWrite(2,a); // see Figure 9 to see a-g
digitalWrite(3,b);
digitalWrite(4,c);
digitalWrite(5,d);
digitalWrite(6,e);
digitalWrite(7,f);
digitalWrite(8,g);
}

// The loop() function will be called over-and-over, forever!
void loop()  { 

//display(ldrValue);  // display 0, then 1, then 2... then 9.
// count from 0 to 9 each time the loop() function is called
int count = 0;
while(true){
ldrValue = analogRead(ldrPin);
ldrValue = map(ldrValue, 0, 700, 0, 9); // Map to 700 as that was around the highest we got the LDR to go
if (ldrValue >= 5){
  count +=1;
}
else {
  count-=1;
}
if (count > 9){
  count = 0;
}
else if (count < 0){
  count = 9;
}
display(count);
Serial.println(ldrValue);
delay(1000); // wait 1 second between each count
}
}
```