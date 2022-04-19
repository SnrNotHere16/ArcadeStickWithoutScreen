The following is a 16 button arcade stick using the tiva TM4C123GXL microcontroller.
# 16 Button Arcade Stick with Analog thumb Joystick
This project  is a 16 button Arcade Stick with an Analog thumb Joystick. This project was cloned from my former project, which was a 15 button controller with a LCD screen. This project was made to add more buttons and make it more easier for people to use and implement.
https://github.com/SnrNotHere16/ArcadeStickWithScreen

<img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/15ButtonArcadeStick.jpg" width= "500" >

Buttons/Ports   <br /> 
 Button0 - PB0  <br />
 Button1 - PB1  <br />
 Button2 - PB2  <br />
 Button3 - PB3  <br />
 Button4 - PB4  <br />
 Button5 - PB5  <br />
 Button6 - PB6  <br />
 Button7 - PB7  <br />
 Button8 - PC4  <br />
 Button9 - PC5  <br />
 Button10 - PC6 <br />
 Button11 - PC7 <br />
 Button12 - PA2 <br />
 Button13 - PA3 <br />
 Button14 - PA4 <br />
 Button15 - PA5 <br />
 AnalogX - PE3 <br />
 AnalogY - PE2 <br />
 AnalogZ - PE1 <br />

# Testing inputs
 The best way to test the inputs is to type "Set up USB game controllers" into the windows search bar. This should prompt this screen. 
 
 <img src = "ArcadeStickImages/HIDScreen.jpg" width= "500" >
 
 Pressing the buttons and moving the thumbstick should be read by the screen. 
 
  <img src = "ArcadeStickImages/DriverImage.jpg" width= "500" >
  
 # Schematic
 Schematic: https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/Schematic_PCB/16buttonTivaCGamepadSchematic.pdf
 <img src = "https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/ArcadeStickImages/CircuitMakerSchematic.PNG" width= "500" >
 
 # Additional Images

 
 # Simple Setup
1. Open LM Flash Programmer
  <img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/LMFlashPlayer.PNG" width = "100">
2. Select TM4C123G LaunchPad 
 <img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/Configuration.PNG" width = "300">
3. Make sure you Tiva c is connected and in DEBUG mode. Go to "Program" and place the bin file ("16button_usb_dev_gamepad.bin"), which is located in this repository, in "Select .bin file" and click "Program"
  <img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/BinProgram.png" width = "300">
4. Disconnect the tiva c and connect it in DEVICE mode. To see if the installation is succesful, type "Set up USB game controllers" into the windows search bar. This should prompt this screen. The tiva c should flash it's green LED. 
   <img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/HIDScreen.jpg" width= "500" >
   <img src = "https://github.com/SnrNotHere16/ArcadeStickWithScreen/blob/master/ArcadeStickImages/GreenLED.jpg" width= "500" >
  
 # Code Composer Project Setup 
 1. In Code Composer Open "Resource Explorer" and select "EK-TM4C123GXL"
 <img src = "https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/ArcadeStickImages/ResourceExplorer.PNG" width= "500" >
 2. Add "usb_dev_gamepad". This is a starter project that uses only 2 buttons (PF0 and PF2), which are the onboard switches. You can run it and test it. If you want to test it, make sure once you load the project to switch the tiva-c to DEVICE mode. You should see the LED blink BLUE. 
<img src = "https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/ArcadeStickImages/ResourceExplorer1.PNG" width= "500" >
<img src = "https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/ArcadeStickImages/ResourceExplorerNew.PNG" width= "500" >
Original project running 
<img src = "https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/blob/master/ArcadeStickImages/BlueLED.jpg" width= "500" >
3. If you would like to run this repository's project. You need to modify four files. Copy and paste the code from these files to the matching files in the starter project.
   https://github.com/SnrNotHere16/ArcadeStickWithoutScreen/tree/master/usb_dev_gamepad_files_changed/usb_dev_gamepad_altered_code
   
4. Build and load the program then switch to device mode. This time the green LED should flash instead of the blue LED. 
