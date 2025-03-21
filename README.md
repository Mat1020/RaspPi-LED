# Controlling LED with Raspberry Pi GPIO
A repositorie to control any color or more than one LED with your Raspberry Pi. From this repositorie, it'll guide and teach you from everything you need to know about LEDs. From how to get started with LEDs with your Raspberry Pi in a begginer project, to how to do fancy circuits with LEDs with your Raspberry Pi, all in step-by-step.

This repositorie should be compadable to every version of Raspberry Pi. 

Without any further do, let's dive in! :D

## Overview
**<u>What is an LED?</u>**
The LED is short for Light Emitting Diode, and it's a semiconductor device that emits light when an electric current passes through it.

There are different types of folders in this repo, for different purposes. You can click on one of the folders: it tells you what materials you need, follow the steps and copy the code to your Raspberry Pi.

# What is a LED?
LED stands for Light Emitting Diode, and it's a semiconductor device that emits light when
an electric current passes through it.

## Tutorial 1: Make an LED blink (in Python)
1 ) Materials:
   
- 1x LED
- 2x Female/Male Jumpers
- 1x Resistor 100 ohn
- Breadboard
- Raspberry Pi
- Micro SD Card
  
2 ) Building the Circuit:

**Step 1:** <br>
Connect one of the female/male jumper to the GND pin
 
**Step 2:** <br>
Connect another female/male jumper to the GPIO 17 pin

**Step 3:** <br>
Connect the GND jumper to the negative row of the breadboard (Right Side)

**Step 4:** <br>
Connect the GPIO 17 jumper to the positive row of the breadboard (Right Side)

**Step 5:** <br>
Grab your LED and connect it to the negative row and the 25 column (Right side)

**Step 6:** <br>
Grab your resistor and connect it to the positive row and the 25 column (Right Side)

3 ) Set Up the Code:

You need to import the LED module:
<pre>
from gpiozero import LED
</pre>

Create a variable named "led" and attach the "LED(17)" value to it:
<pre>
led = LED(17)
</pre>

The 'led.on()' method turns on the LED:
<pre>
led.on()
</pre>
   
The 'led.off()' method turns off the LED:
<pre>
led.off()
</pre>

The 'led.toggle()' method turns on if it was off and vice versa:
<pre>
led.toggle()
</pre>

4 ) My Program Examples:

A. led_flash.py <br>
This Python script is making the LED blink (turn on and off) for 5 times with a 0.5-second sleep in between. 
