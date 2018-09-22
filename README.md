# Paper Puppets

*A lab report by Tal Genkin*

## Part A. Actuating DC motors

[Vibrating Motor](https://youtu.be/gCBmTMZoDb8)

## Part B. Actuating Servo motors

### Part 1. Connect the Servo to your breadboard

**a. Which color wires correspond to power, ground and signal?**

Red goes to 5V (power), yellow goes to pin 9, and brown goes to Ground. 

### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

Pin number 9, as defined in the code:

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

**b. What aspects of the Servo code control angle or speed?**

This part of the code tells the motor to go from 0 to 180 degrees while also delaying it (goes 90 degrees to each side):

int pos = 0;    // variable to store the servo position

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}

## Part C. Integrating input and output

[Motor](https://www.youtube.com/watch?v=VN606gDgFkU&feature=youtu.be)

[Motor moving slower](https://youtu.be/i6GQygcZe2Q)

## Part D. Paper puppet

**a. Make a video of your proto puppet.**

[Puppet in action](https://youtu.be/i2X0khBci9Q)

## Part E. Make it your own

**a. Make a video of your final design.**
 
