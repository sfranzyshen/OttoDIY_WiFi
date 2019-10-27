# OttoDIY WiFi
*Addon for the OttoDIY opensource Project. http://ottodiy.com*

## Motivation for the project

When developing with the OttoDIY Robot a few things can get in the way and sometimes make it difficult or even lead to failure. 

The first *(and most obvious)* is the need to install software and possibly hardware drivers onto a device before you can do anything. Downloading software from various sources and for a variety of platforms ... can be confusing. Also, not everyone has access to the needed files ... or sometime the files are not for their available platform.

The second obstacle to OttoDIY development is the need to code, compile, and upload changes to the robot ... Yes, you could use mBlock to do "Live" coding ... but ultimately if you want your code to run stand alone ... You'll need to code, compile, and upload your changes to the OttoDIY Robot ...

Another inhibiting *(and the most annoying)* tether is the USB cable. What else can I say about it? Unless it's used to recharge the battery ... we are going to ditch it and go full wireless. *(And not just a remote control ...)*

## What can we do about it?

The idea is to replace the Bluetooth module with a WiFi module and not just any WiFi module but explicitly the ESP8266 (ESP8285). This WiFi module is so much more ... it's also a fully programmable micro-controller. *(just like the Arduino Nano ... even more power)* By adding this second micro-controller we will not only be able to add WiFi connectivity ... but we will also be able to add additional functionality  ... creating a OttoDIY Robot "Buddy" doing stuff like ...

- Updating *(uploading)* the Nano's firmware from the ESP over WiFi or from a default firmware image stored on the ESP's flash ... 
- Provide a web based user interface similar to that of the Android App ... 
- Add a *(off-line)* web based Blockly editor with  "Live Coding" interface similar to the mBlock addon ... 
- Store *(Blockly Scripts)* programs on the ESP's flash ... 
- Interpret stored programs and control the nano using the existing *(Serial)* remote-control interface allowing for development without compiling and uploading code.
- Add a network wide protocol to provide syncronized danceing over mutilple otto's.
- Add MP3 audio playback of files stored on the ESP's flash ...
- and more ...

## Out-Of-The-Box

Imagine our ESP module is (pre)programmed with our project and has a default copy of the OttoDIY firmware and a built in web application *(IDE)* stored on it's internal flash *(SPIFFS)* ... In theory we would be able to add a "blank" Nano to our build, and from the web based user interface, upload the default firmware to the Nano ... bootstrapping our OttoDIY Robot integrated development environment ... We can connect *(Wireless)* from ANY device that has a web browser and WiFi connectivity ... without ever needing internet access ... nor installing any software on the connecting device ... We would be able to immediately *(using the various web interfaces)* "Out-Of-The-Box" control and interact with our OttoDIY Robot.

## Questions?
If the object is to teach the Arduino work-flow stack, aren't you eliminating the the Arduino environment completely with the Blockly/Interpreter Web App approach?

Yes and No. Yes it's true there isn't a functional Interpreter for the Arduino C++ environment, but the Blockly interface can generate real Arduino code *(That can be used with the normal Arduino IDE)* as well as the LUA code that is used for the builtin script Interpreter. Also, we maybe able to add the ability to use the Arduino IDE to upload sketches wireless(ly) providing a path from the Blocky environment to the Arduino IDE environment for students.

## OK, Where is the code?

# References
- https://github.com/OttoDIY
- https://wikifactory.com/+OttoDIY
