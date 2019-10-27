# OttoDIY WiFi
*Addon for the OttoDIY opensource Project. http://ottodiy.com*

## Motivation for the project

When developing with the OttoDIY Robot a few things can get in the way and sometimes make it difficult or even lead to failure. 


The first *(and most obvious)* is the need to install software and possibly hardware drivers onto a device before you can do anything. Downloading software from various sources and for a variety of platforms ... can be confusing. Also, not everyone has access to the needed files ... or sometime they are not for the available platform.


The second obstacle to OttoDIY development is the need to code, compile, and upload changes to the robot ... Yes, you could use mBlock to do "Live" coding ... but ultimately if you want your code to run stand alone ... You'll need to code, compile, and upload your changes to the OttoDIY Robot ...


Another inhibiting *(and the most annoying)* tether is the USB cable. What else can I say about it? Unless it's used to recharge the battery ... we are going to ditch it and go full wireless. *(Not just a remote control ...)*

## What can we do about it?

The idea is to replace the Bluetooth module with a WiFi module and not just any WiFi module but explicitly the ESP8266 (ESP8285). This WiFi module is so much more ... it's also a fully programmable micro-controller. *(just like the Arduino Nano ... even more power)* By adding this second micro-controller we will not only be able to add WiFi connectivity ... but we will also be able to add additional functionality ... 

- Such as updating *(uploading)* the Nano's firmware from the ESP over WiFi or from a default firmware image stored on the ESP's flash ... 
- Provide a web based user interface similar to that of the Android App ... 
- Add a *(off-line)* web based Blockly editor with  "Live Coding" interface similar to the mBlock addon ... 
- Store *(Blockly Scripts)* programs on the ESP's flash ... 
- Interpret programs and control the nano using the existing remote-control interface allowing development without compiling and uploading code.

## OK, Where is the code?


# References
- https://github.com/OttoDIY
- https://wikifactory.com/+OttoDIY
