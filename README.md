# Controlling LED with Raspberry Pi GPIO
A repositorie to control any color or more than one LED with your Raspberry Pi. From this repositorie, it'll guide and teach you from everything you need to know about LEDs. From how to get started with LEDs with your Raspberry Pi in a begginer project, to how to do fancy circuits with LEDs with your Raspberry Pi, all in step-by-step.

This repositorie should be compadable to every version of Raspberry Pi. 

Without any further do, let's dive in! :D

## Overview
**What is an LED? What are LEDs used for?** <br>
The LED is short for Light Emitting Diode, and it's a semiconductor device that emits light when an electric current passes through it. LEDs are used for various purposes, including: lighting fixtures, displays, automotive lighting, and even medical equipment because due to their energy efficiency, long lifespan, and versatility.

**What does GPIO stand for?** <br>
Raspberry Pi GPIO pins stand for _General Purpose Input/Output_. They are used to connect with the outside world and physical objects, and they are located on the edge of the Raspberry Pi board.

**Summary** <br>
We're going to use the Raspberry Pi GPIO pins to control the LED(s). We're going to use gpiozero module from Python to write the code, and we're going to need basic materials for the projects.

## Table of Contents
You can click on the link to go to the project you're interested in. The projects go from **easiest** to **hardest**.

- [Project #1: Make an LED Blink](#project-1-make-an-led-blink)

## BEFORE Building Up the Circuit
**Raspberry Pi GPIO Pinout Diagram** <br>
Before connecting and setting anything yet, you need to understand what the pinout of your Raspberry Pi is. The Raspberry Pi GPIO pinout diagram shows you the **name of each pin** and  **information about the functions of each pin**.

You can find your Raspberry Pi GPIO pinout diagram by typing in your broswer search:

<pre>
________________ gpio pinout
</pre>

In the blank, type your Raspberry Pi version.

For example, this Raspberry Pi GPIO pinout diagram correspons to **Raspberry Pi 4** (I couldn't find the orginal image):
![cc865253-a2ad-47f6-84ac-4d4b0d6870e1](https://github.com/user-attachments/assets/89ba31d4-9e08-4d9a-b6da-f717cf7cc9cb)

**LED Layout** <br>
As you may have noticed or not, LEDs have two legs corresponding to either negative energy or positive energy. The **positive** leg is usually the one who is the **longest**, and the **negative** is the **shortest**. Below, there's an image showing what leg correspons to:
![db2e19eb-96a6-4caa-ba82-68efb21a3f36](https://github.com/user-attachments/assets/39a64e84-8301-4dfa-8065-61fde7802af4)

# Project #1: Make an LED Blink
This project is making the LED blink (turns on and off) for 5 times with a 0.5-second sleep in between. This project is great for begginers who want to get stated into using their Raspberry Pi into awesome project ideas. 

Keep in mind that **you should play and mess with it**, meaning that **you should be changing stuff (after you are done with the project) to explore and discover more**. 

## Materials
**Components** <br>
- 1x LED
- 2x Female/Male Jumpers
- 1x 100 ohm Resistor

**Tools/Equipment** <br>
- Raspberry Pi
- Micro SD Card
- Breadboard
  
## Bulding Up the Circuit
1. Connect one of the Female/Male Jumper to the GND pin.

2. Connect another Female/Male Jumper to the GND pin.

3. Connect the GND jumper to the negative row of the breadboard (Right Side).

4. Connect the GPIO 17 jumper to the positive row of the breadboard (Right Side).

5. Grab your LED and connect it to the negative row and the 25 column (Right side).

6. Grab your resistor and connect it to the positive row and the 25 column (Right Side).

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
