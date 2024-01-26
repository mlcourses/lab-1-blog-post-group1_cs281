  # Lab 1: Intro to Hardware!

## Overview and Motivation
This week we'll explore digital circuits and the hardware we will be using in this course. We will be introduced to PB-503 breadboard prototyping stations and about the Arduino, which is a a microcontroller system for supporting embedded processor control. We will understand how to work with circuit components such as LEDs, resistors and logic gates built into ICs.

## Materials
1. PB-503
2. Arduino Kit
3. Basic LED Circuts
4. Logic Gates Ex: 7404 Inverter, 7408 AND
5. Wires
6. Resistors
7. It is important to handle these devices carefully!

## Lab Objectives
1. Breadboard Proficiency
2. Digital Circuit Construction
3. Logic Gates and ICs
4. Arduino Integration
## Project Steps

## Breadboard Proficiency
For the first part of the lab, we experimented with a breadboard to understand their use. We began by exploring the breadboard and indentifying connections on the board, specically how the holes are wired, using the GND and +5V terminals. We saw how the holes in the top 4 rows, the top 2 rows are wired to each other, and the bottom 2 rows are wired to each other. Thus, the top 2 rows were wired to +5V, while the bottom 2 were wired to GND. Also, when a +5 volt wire was connected to a row of 5 holes, it would give voltage to the rest of the row. When a +5V wire was connected to the column with only 2 holes per row, it would give voltage to the same column. When we used the logic indicators, we found this hypothesis to be correct. 



![IMG_4217](https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/97915038/f4fc5924-d990-4621-a040-b4bb2190bfbd)





The high indicates that the wire is connected to +5 Voltage while low is connected to ground. After this we began to build our own digital circuit. To get it to work, we first connect the LED short leg to GND and put the long leg to same row as a resistor. We then connect a resistor in the same row as a wire to give the LED power and use the resistor to limit excess current that can harm the LED.

## Digital Circuit Construction



https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/97915038/cc2c551f-6f29-4986-ac39-523363f4f53a



Connecting the circut with the function generator can change alot about the LED light. For example, by changing the frequency using the left slider from 1.0 to .1 change how fast the light lights up. The amp contols how bright the light gets. Also changing the frequency from 1 to 10 to even 100 switches the amount of cycles per second.

## Logic Gates and ICs

Next we started to work with Logic gates and IC's. The first IC we began using is 7404 Inverter with the function generator to show the inversion between 1A and 1Y. 


https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/04892b08-bc76-4536-af18-b9adff71059e


Next we took a 7408 AND Gate to show that both switches must be on to show the AND operation working. As described in the video, when both swithces are off or only one is on, the logic indicators shows low. When they are both 1 the logic indicator is high.





https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/2bc64894-7ff1-47fc-81d4-38fd9c827e6c

## Arduino Integration

Lastly we used the Arduino which is a embedded controller. We learned that the Arduino can be used to specify a behavior in a circuit. By connecting it to our computer and using the code below, we learned that this code includes three varibles. P which is a digital pin, and A and B being the amount of time in milliseconds that the LED will be delayed.

```
const int P = 13;
const int A = 1000;
const int B = 1000;

void setup() {
  // put your setup code here, to run once:
  pinMode(P, OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(P, HIGH);
  delay(A);
  digitalWrite(P, LOW);
  delay(B);
}
```

The function setup() initialized P as the output using pinmode() meaning that the wire connecting the arduino must be 13. A and B are used in the loop function which delays the LED light for 1000 milliseconds. The loop repeatedly turns on the LED for 1000 miliseconds using digitalWrite and then turns the LED off(low) for 1000 milliseonds for an infinite loop.


https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/4706ba2d-a453-49b4-a785-ef82f415003e





## Conclusion

Lab 1 gave us an introduction to hardware components and digital circuits. We started of by familiarizing ourself with the breadboard and discovering connections between GND and +5V. We built a digital circuit, learning how to properly operate with LEDs and observing the effects of the function generator. We experimented with Logic Gates and ICs demonstrating inversion and the AND gate using logic indicators. Lastly we utilized Arduino to specify the circuit behavior and learned about the code behind it.




