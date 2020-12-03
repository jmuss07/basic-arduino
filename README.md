# basic-arduino\# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)

## HelloArduino

### Description & Code

```C++

int ledPin1 = 12;
int ledPin2 = 13;

void setup() {
  // put your setup code here, to run once:
  pinMode(ledPin1, OUTPUT);//This sets the digital pin as the output
  pinMode(ledPin2, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:

 Serial.println("Blink");

  digitalWrite(ledPin1, HIGH); //turns led 1 on
  digitalWrite(ledPin2, LOW); // turns led 2 off
  delay(300);
  digitalWrite(ledPin1, LOW); //turns led 1 off
  digitalWrite(ledPin2, HIGH); //turns led 2 on
  delay(300);
}
//I reused my code from last year, but was mildly unsure as to how to make it fade, so i just used 2 leds instead and made them alternate.
```

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/jmuss07/949017d6-c491-49d1-a9a4-9ee524bd7a4c)

### Image or Wiring
...wiring diagram coming soon...

### Reflection
I realised that I had the basic code from last year, so I used that. However, I couldn't figure out how to make it fade, so I used two LEDs and made them aternate blinking.

## FiniteLEDBlink

### Description & Code

```C++
/*

*/
int LED = 13; //sets the led as a variable, as well as gives it a pin to run through
int blink = 0; //sets the counter
void setup() {
  pinMode(LED, OUTPUT);
  Serial.begin(9600); //starts the serial moniter
}

void loop() {
  if (blink < 6){ //function runs if the counter is less than 6
  Serial.println("Blink!!:D"); //prints out a line for the serial moniter, tells you that the led is blinking
  digitalWrite(LED, HIGH); //turns the led on
  delay(1000); 
  digitalWrite(LED, LOW); //turns the led off
  delay(1000);
  blink++; //adds to the counter
  }
  else { //if the counter is greater than or equal to 6...
    Serial.println("Nope!"); //print "Nope!" on the serial moniter, tells you that counter is greater than or equal to 6
    digitalWrite(LED, LOW); //turns led off
  }
}
```

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/jmuss07/040ed7ab-7817-441c-922b-a898b5f45035)

### Image or Wiring
...wiring diagram coming soon...

### Reflection
This assignment was fairly simple to create, though I had trouble adding to the counter at first. In the end, I went to the arduino website, which explained how to add to the counter.
