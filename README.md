# OttoDIY_WiFi
*Addon for the OttoDIY opensource Project. http://ottodiy.com*

## Motivation for the project

When developing with the OttoDIY Robot a few things can get in the way and sometimes make it difficult or even lead to failure. 

**The first** *(and most obvious)* is the need to install software and possibly hardware drivers onto a device before you can do anything. Downloading software from various sources and for a variety of platforms ... can be confusing. Also, not everyone has access to the needed files ... or sometime the files are not for their available platform.

**The second** obstacle to OttoDIY development is the need to code, compile, and upload changes to the robot ... Yes, you could use mBlock to do "Live" coding ... but ultimately if you want your code to run stand alone ... You'll need to code, compile, and upload your changes to the OttoDIY Robot ... over and over again.

**Another inhibiting** *(and the most annoying)* tether is the USB cable. What else can I say about it? Unless it's used to recharge the battery ... we are going to ditch it and go full wireless. *(And not just a remote control ...)*

## What can we do about it?

The idea is to replace the Bluetooth module with a WiFi module and not just any WiFi module but explicitly the ESP8266 (ESP8285). This WiFi module is so much more ... it's also a fully programmable micro-controller. *(just like the Arduino Nano ... even more power)* By adding this second micro-controller we will not only be able to add WiFi connectivity ... but we will also be able to add additional functionality  ... creating a OttoDIY Robot "Buddy" doing stuff like ...

- Updating *(uploading)* the Nano's firmware from the ESP over WiFi or a default firmware image stored on the ESP ... 
- Provide a web based user interface similar to that of the Android App ... with calibration
- Add a *(off-line)* web based Blockly editor with  "Live Coding" interface similar to the mBlock addon ... 
- Store *(Blockly Scripts)* programs on the ESP's flash ... 
- Interpret stored programs and control the Nano using the existing *(Serial)* remote-control interface allowing for development without compiling and uploading code. Restarts stored program on power cycles.
- Add a network wide protocol to provide syncronized dancing over mutilple otto's ...
- Add MP3 audio playback of files stored on the ESP's flash ...
- and more ...

## Out-Of-The-Box

Imagine our ESP module is (pre)programmed with our project and has a default copy of the OttoDIY firmware and a built in web application *(IDE)* stored on it's internal flash *(SPIFFS)* ... In theory we would be able to add a "blank" Nano to our build, and from the web based user interface, upload the default firmware to the Nano ... bootstrapping our OttoDIY Robot with a built in integrated development environment ... We could connect *(Wireless)* from **ANY** device that has a web browser and WiFi connectivity ... without needing to connect to the internet ... nor installing any software on the connecting device being used ... We would be able to immediately *(using the various web interfaces)* control and interact with our OttoDIY Robot **"Out-Of-The-Box"**.

## Questions?
>**If the objective is to teach the Arduino *(work-flow)* IDE ... aren't you eliminating the the Arduino environment completely with the Blockly/Interpreter/Web App approach?**

**Yes and No.** Yes it's true that there isn't a functional interpreter for the Arduino C++ environment, but the Blockly interface can generate real Arduino code *(That can be used with the normal Arduino IDE)* as well as the LUA code that is used for the internal script interpreter. We may be able to add the ability to use the Arduino IDE to upload sketches **wireless(ly)** providing students a pathway from the Blockly *(bulitin)* environment ... to the regular Arduino IDE environment. 

>**Why add a second microcontroller ... why not do everything from the ESP and drop the Nano?**

**This is a great question!** We have also given this some great thought ... however there are several considerations that have to be addressed ...

The **first** thing is the hardware. One of the advantages to the OttoDIY Robot is the low cost, and the using of relatively available standard components ... But we have not been able to identify a suitable replacement for the Nano expansion board ... and therefore it would be required to make a custom board ... where to start ... but more importantly ... where to stop ...

**Second** we want to maintain the **"Interpreted Environment"** so that we don't have to perform code, compile, upload cycles. The interpreter can handle both methods. Either controlling the local hardware directly *(with just the ESP)* or using the serial bridge to control the Nano ... So there is a direct migration once the hardware board is completed ... and this is within the scope of this project ... and we expect to provide both firmwares *(One for two micro-controllers and one for everything on an ESP)*

**Alternatively** as mentioned in the question above ... the script interpreter we use for **this** project is the LUA language ... that isn't usually used as a teaching language  ...  A more modern *(applicable)* programming language would be python ... but of the python implementations available for the ESP platforms all are **"bare-metal"** based and would  require either a port of python to the Arduino environment ... or a full port of the OttoDIY Robot API to a python based platform. We have started a separate project to explore this very idea ... https://github.com/sfranzyshen/OttoDIY_Python


## OK, Where is the code?

We are currently still organizing and planning ... https://github.com/sfranzyshen/OttoDIY_WiFi/tree/develop

# References
- https://github.com/OttoDIY
- https://wikifactory.com/+OttoDIY

make a change
