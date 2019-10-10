# Paper Puppets

*A lab report by John Q. Student*

## In this Report

To submit your lab, clone [this repository](https://github.com/FAR-Lab/IDD-Fa18-Lab4). You'll need to describe your design, include a video of your paper display in operation, and upload any code you wrote to make it move.

## Part A. Actuating DC motors

[Video for Actuating DC Motors](https://youtu.be/RPXtr2WpElo)

## Part B. Actuating Servo motors

### Part 1. Connect the Servo to your breadboard

**a. Which color wires correspond to power, ground and signal?**

The brown wire corresponds to Ground.
The red wire corresponds to Power.
The orange wire corresponds to Signal.

### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

The signal line of the servo should be connected to pin 9 on the Arduino

**b. What aspects of the Servo code control angle or speed?**

The lines that have the function myservo.write(pos) control the angle. 

The lines that have 'delay(AMOUNT)' control the speed, with a smaller AMOUNT making the motor go faster. 

```
#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(10);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(10);                       // waits 15ms for the servo to reach the position
  }
}
```

## Part C. Integrating input and output

**Include a photo/movie of your raw circuit in action.**

[Link to video](https://youtu.be/fT_uWJnWUjs)

## Part D. Paper puppet

**a. Make a video of your proto puppet.**

[Link to video of paper puppet](https://youtu.be/woOBmVv1HZs)

## Part E. Make it your own

**a. Make a video of your final design.**

[Link to video of finale design of good kiddo](https://youtu.be/qqW4fb8mtjk)

[Code for Part E](https://github.com/sgc87/IDD-Fa19-Lab4/blob/master/Lab4.ino)
 
