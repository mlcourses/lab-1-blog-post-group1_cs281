  # Lab 1: Intro to Hardware!

## Overview and Motivation
This week we'll explore digital circuits and the hardware we will be using in this course. We will be introduced to PB-503 breadboard prototyping stations and about the Arduino, which is a a microcontroller system for supporting embedded processor control. We will understand how to work with circuit components such as LEDs, resistors and logic gates built into ICs.

## Materials
1. PB-503
2. Arduino Kit
3. Basic LED Circuts
4.Logic Gates Ex: 7404 Inverter, 7408 AND
5. Wires
6. Resistors
## Project Steps
For the first part of the lab, we experimented with a breadboard to understand their use. We began by exploring the breadboard and indentifying connections on the board specically GND and 5V and finding patterns. We saw how the wires that were connected to the top row contained +5 Volts while to lower row contained GND. Also when a +5 volt wire was connected to a group with a column of 5 below it would give voltage to the rest of the row. When a +5 wire was connected to the group with two columns, it would give voltage to the same row. When we used the logic indicators, we found this hypothesis to be correct. 

https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/49ac72b3-e3b8-4da4-8803-32981dcfd888

The high indicates that the wire is connected to +5 Voltage while low is connected to ground. After this we began to build our own digital circuit. To get it to work, we first connect the LED to GND and put the other end to same row as a resistor. We then connect a resistor in the same row as a wire which is connected to +5 V.

## Digital Circuits

https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/97915038/70750896-6a0b-4fd4-82d4-97ca9856c7a9

Connecting the circut with the function generator can change alot about the LED light. For example, by changing the frequency using the left slider from 1.0 to .1 change how fast the light lights up. The amp contols how bright the light gets. Also changing the frequency from 1 to 10 to even 100 switches the amount of cycles per second.

Next we started to work with Logic gates and IC's. The first IC we began using is 7404 Inverter to show the inversion between 1A and 1Y. Next we took a 7408 inverter to show that both switches must be on to show the AND operation working.


https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/04892b08-bc76-4536-af18-b9adff71059e








https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/2bc64894-7ff1-47fc-81d4-38fd9c827e6c



Lastly we used the Arduino which is a embedded controller. We learned that the Arduino can be used to specify a behavior in a circuit. By connecting it to our computer and using the code below, we learned that this code includes three varibles. P which is a digital pin, and A and B being the amount of time in milliseconds that the LED will be delayed.

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

https://github.com/mlcourses/lab-1-blog-post-group1_cs281/assets/112486168/4706ba2d-a453-49b4-a785-ef82f415003e





## Conclusion




