# ESP8266 dual edge wake

This module will wake an ESP8266 from deep sleep when a sensor value changes (e.g. push button, float sensor, or other reed sensor). 

<img width="382" alt="Screenshot 2023-01-29 at 23 00 59" src="https://user-images.githubusercontent.com/313427/215360613-dd6d202e-2c78-45f2-ac10-465c2957697e.png">

When the input goes from high to low or low to high, a short pulse is generated on the output. 

![mnL7V](https://user-images.githubusercontent.com/313427/215360746-bf435abf-e21a-4aa5-8b4a-81841f77af7a.png)

![MbJCn](https://user-images.githubusercontent.com/313427/215360752-3640857b-7d23-4961-aad8-e682eb83f012.png)

Either circuit A or B can be used. A is a dual edge monostable trigger, and B is an edge to glitch conveter (XOR with delay). 
Solder the circuit jumper to choose between circuit A or B (the center pad is the input). 

For circuit A, solder either the leading or falling jumper (or both can be soldered to pulse on both edges).
For circuit B, a pulse will always be generated on both edges.
