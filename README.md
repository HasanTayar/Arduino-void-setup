# Arduino-void-setup

# Blink LED

This code blinks an LED connected to pin 3 of an Arduino board.

## Requirements
1. Arduino board
2. LED
3. Jumper wires
## Usage
1. Connect the anode (+) of the LED to pin 3 of the Arduino board.
2. Connect the cathode (-) of the LED to ground (GND) of the Arduino board.
3. Upload the code to the Arduino board.
4 .The LED should start blinking at a rate of one second on and one second off.
## Code 1: Blink LED
```C#
void setup()
{
  pinMode(3, OUTPUT);
  digitalWrite(3, HIGH);
  delay(3000);
}

void loop()
{
  digitalWrite(3, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(3, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```
## Switch Controlled LEDs
This code turns on or off LEDs connected to pins 8, 9, and 10 of an Arduino board based on the state of switches connected to pins 5, 4, and 3.

## Requirements
1. Arduino board
2. 3 switches
3. 3 LEDs
4. Jumper wires
## Usage
1. Connect one terminal of each switch to ground (GND) of the Arduino board.
2. Connect the other terminal of each switch to pins 5, 4, and 3 of the Arduino board.
3. Connect the anodes (+) of each LED to pins 8, 9, and 10 of the Arduino board.
4. Connect the cathodes (-) of the LEDs to ground (GND) of the Arduino board.
5. Upload the code to the Arduino board.
6. The LEDs should turn on or off based on the state of the switches.

## Code 2: Switch Controlled LEDs
```C#
void setup() {
  pinMode(5, INPUT_PULLUP);
  pinMode(4, INPUT_PULLUP);
  pinMode(3, INPUT_PULLUP);
  pinMode(2, INPUT_PULLUP);
  
}

void loop() {
  if(digitalRead(5)==0){
    if(digitalRead(4)==0){
      digitalWrite(8,HIGH);
    }
    else{
       digitalWrite(8,LOW);
    }
      if(digitalRead(3)==0){
      digitalWrite(9,HIGH);
    }
     else{
       digitalWrite(9,LOW);
    }
      if(digitalRead(2)==0){
      digitalWrite(10,HIGH);
    }
     else{
       digitalWrite(10,LOW);
    }
    
    
  }
  else{
     digitalWrite(8,LOW);
     digitalWrite(9,LOW);
     digitalWrite(10,LOW);
  }
}

```
## 7-Segment Display
This code displays a number on a 7-segment display using pins 2, 3, 4, 5, 6, 12, and 13 of an Arduino board.

## Requirements
1. Arduino board
2. 7-segment display
3. Jumper wires
4. Usage
5. Connect each segment of the 7-segment display to its corresponding pin on the Arduino board (a to pin 2, b to pin 3, c to pin 4, and so on).
6. Connect the common cathode (-) of the 7-segment display to ground (GND) of the Arduino board.
7. Upload the code to the Arduino board.
8. Call the turnOn function with a number between 0 and 9 to display that number on the 7-segment display.
## Code 3: 7-Segment Display
```C#
void setup()
{
 
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(13, OUTPUT);
 
  turnOn(9);

}

void loop()
{
}

void turnOn(int num)
{
   if(num == 0)
  {
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
  }
  if(num == 1)
  {
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
  }
  if(num == 2)
  {
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(5,HIGH);
  }
  if(num == 3)
  {
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
  }
   if(num == 4)
  {

    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(4,HIGH);
  }
   if(num == 5)
  {

    digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
  }
   if(num == 6)
  {

	digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
  }
  
  if(num == 7)
  {

    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);

  }
    if(num == 8)
  {

	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);

  }
  
      if(num == 9)
  {

    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);

  }
  
}

```
## Counting 7-Segment Display
This code displays numbers from 0 to 9 and then from 9 to 0 on a 7-segment display using pins 2, 3, 4, 5, 6, 12, and 13 of an Arduino board.

##Requirements
1. Arduino board
2. 7-segment display
3. Jumper wires
## Usage
1. Connect each segment of the 7-segment display to its corresponding pin on the Arduino board (a to pin 2, b to pin 3, c to pin 4, and so on).
2. Connect the common cathode (-) of the 7-segment display to ground (GND) of the Arduino board.
3. Upload the code to the Arduino board.
4. The code will continuously display numbers from 0 to 9 and then from 9 to 0 on the 7-segment display.
```C#
void setup()
{
 
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(13, OUTPUT);


}

void loop()
{
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
	
  	delay(1000);
	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);	
  
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
	
  	delay(1000);
	
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(5,HIGH);

 	delay(1000);
  	
  		digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
    digitalWrite(2,HIGH);
	digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
 
	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
	digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(4,HIGH);
	
  	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);

	digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
	
  	delay(1000);
  	
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  
	digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
	
  	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);

	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);

  	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);

	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);
	delay(1000);
  
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  
  	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);
 	delay(1000);
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
   	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
  	delay(1000);
  	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  	digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
  	delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  	
  	digitalWrite(2,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
  	delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(13,HIGH);
    digitalWrite(4,HIGH);
    delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(5,HIGH);
    delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
    delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
  
  
  	digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
    digitalWrite(5,HIGH);
    digitalWrite(6,HIGH);
    digitalWrite(13,HIGH);
    delay(1000);
 	digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
    digitalWrite(6,LOW);
    digitalWrite(13,LOW);
  	digitalWrite(12,LOW);
 }
```
## Authors
[Hasan Tayar](https://github.com/HasanTayar "Hasan Tayar")
