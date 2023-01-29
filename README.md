# ESP8266 dual edge wake

This module will wake an ESP8266 from deep sleep when a sensor value changes (e.g. push button, float sensor, or other reed sensor). 

<img width="382" alt="Screenshot 2023-01-29 at 23 00 59" src="https://user-images.githubusercontent.com/313427/215360613-dd6d202e-2c78-45f2-ac10-465c2957697e.png">

When the input goes from high to low or low to high, a short pulse is generated. 
Either circuit A or B can be used. A is a dual edge monostable trigger, and B is an edge to glitch conveter (XOR with delay). 
