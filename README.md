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
 
_Step 2:_ <br>
Connect another female/male jumper to the GPIO 17 pin

_Step 3:_ <br>
Connect the GND jumper to the negative row of the breadboard (Right Side)

_Step 4:_ <br>
Connect the GPIO 17 jumper to the positive row of the breadboard (Right Side)

_Step 5:_ <br>
Grab your LED and connect it to the negative row and the 25 column (Right side)

_Step 6:_ <br>
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

4 ) My Programs:

A. led_flash.py <br>
This Python script is making the LED blink (turn on and off) for 5 times with a 0.5-second sleep in between. 
