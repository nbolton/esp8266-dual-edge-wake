# ESP8266 dual edge wake

This module will wake an ESP8266 from deep sleep when a sensor value changes (e.g. push button, float sensor, or other reed sensor). 

**Disclaimer:** If you need to do this, then you should probably use a different MCU that supports deep sleep interrupt on edge. But, if like me, you bought many ESP8266s and want to use them in a project where you have this requirement...

Connect input to the sensor, and output to the RST pin on the ESP8266.

<img width="382" alt="Screenshot 2023-01-29 at 23 00 59" src="https://user-images.githubusercontent.com/313427/215360613-dd6d202e-2c78-45f2-ac10-465c2957697e.png">

*Note: Above is Rev 1 (latest is Rev 1a)*

When the input changes (goes from high to low or low to high), a short pulse is generated on the output which wakes the ESP8266 from deep sleep.

![mnL7V](https://user-images.githubusercontent.com/313427/215360746-bf435abf-e21a-4aa5-8b4a-81841f77af7a.png)

Note: The blue line above is mis-labeled as Q1, and should read Q3.

![MbJCn](https://user-images.githubusercontent.com/313427/215360752-3640857b-7d23-4961-aad8-e682eb83f012.png)

Either circuit A or B can be used. A is a dual edge monostable trigger, and B is an edge to glitch conveter (XOR with delay). 
Solder the circuit jumper to choose between circuit A or B (the center pad is the input). 

For circuit A, solder either the leading or falling jumper (or both can be soldered to pulse on both edges).
For circuit B, a pulse will always be generated on both edges.

VCC min 2.5 V, max 6.0 V.

Example use case: Wake your ESP8266 and report a float sensor value change (e.g. when a water tank is full).

![IMG_4267](https://user-images.githubusercontent.com/313427/217043657-98af805b-a553-45fe-a37e-39dfdaa4d4b1.jpg)

*Note: Resistor bodge was needed for board Rev 1 (now obsolete, replaced by Rev 1b which fixed the issue).*
