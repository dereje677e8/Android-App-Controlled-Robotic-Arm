# Android-App-Controlled-Robotic-Arm

The main aim is to make a feasible robotic arm controlled by an android application, which would be portable and flexible. 


                                  MATERIALS USED:
1. Servo Motors 

Servos enable you to accurately control physical movement because they generally move to a
position instead of continuously rotating. They are ideal for making something rotate over a range
of 0 to 180 degrees. Servos are easy to connect and control because the motor driver is built into
the servo.

![image](https://user-images.githubusercontent.com/69731494/190861084-df29e81c-0bf0-44af-bbf7-a0880f9ef006.png)

2. HC-06 Bluetooth Module

HC serial Bluetooth products consist of Bluetooth serial interface module and Bluetooth adapter.
The HC-06 BT module is a slave operating only and uses a serial communication protocol. In
Bluetooth communication, master and slave are determined according to the state of connection
start. A master module can initiate the connection, but the slave module cannot initiate the
connection. In our project, we will provide an external device to connect to a slave PC or an android
device. Bi-directional data can be sent and received in a healthy way. This module can be
configured for baud rates 1200 to 115200 bps.
![image](https://user-images.githubusercontent.com/69731494/190861180-384b5150-b9ab-4b8f-ab10-75c54ec6622f.png)

3. Arduino Uno

The Arduino Uno is based on the ATmega328 (datasheet). It has 14 digital input/output pins (of
which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz ceramic resonator, a USB
connection, a power jack, an ICSP header, and a reset button. It contains everything needed to
support the microcontroller; simply connect it to a computer with a USB cable or power it with a
AC-to-DC adapter or battery to get started. The Uno differs from all preceding boards in that it
does not use the FTDI USB-to-serial driver chip. Instead, it features the Atmega16U2 (Atmega8U2
up to version R2) programmed as a USB-to-serial converter.

![image](https://user-images.githubusercontent.com/69731494/190861325-fde3ac37-e345-42ff-9c06-fd2cba866fa9.png)

                                              HARDWARE IMPLEMENTATION
                                              
The design of the robotic arm structure 3d Printed
 ![image](https://user-images.githubusercontent.com/69731494/190861451-9b63db4f-3c55-4e45-b1f4-15bccf076e29.png)

Circuit Diagram

AACRA basically contains six major hardware parts. These are the Gripper, Wrist Pitch, Wrist
Roll, Elbow, Shoulder and Waist, each of which has their own significance with analogical
importance with the human arm. All these parts of the arm do have their own representation in
both the Arduino code and the developed android application.

![image](https://user-images.githubusercontent.com/69731494/190861511-f098f7e6-98e3-4522-a10e-124f8a2fb368.png)


                                                SOFTWARE IMPLEMENTATION
                                                
The application is developed using android studio which is a software tool provided for android
application development. With the help of this software, we have developed the application for
controlling the robotic arm through a Bluetooth module connected to the Arduino microcontroller.
The application is developed in a such a way that it provides user friendly GUI features. This was
made to make the control scenario much easier for the one who wanted to control the robotic arm.
The application has basically three user interfaces (GUI’s) and a number of varieties of button and
toast messages so that to enhance the use-friendly feature of application.
When the application icon is clicked from the screen of the user’s android device, the first thing
that pops up is the search button that is used to search for any locally available device. Also, on
the action bar the name of the application is shown “ROBO ECE” and an “About us” button is
also displayed which leads to another activity(interface). 

HOME PAGE

![image](https://user-images.githubusercontent.com/69731494/190861920-52aa21f6-12dd-4a30-a6e3-bf2808d78349.png)

If we clicked the button “About us” on the action bar, then a new activity (interface) is opened and
the developers name is displayed. Also, a copy right information is stated at the bottom of the
screen. We can return to the previous activity (interface) by clicking the back button on our android
device.

ABOUT US

![image](https://user-images.githubusercontent.com/69731494/190861983-72786b6d-1f58-4f50-ae43-5652cd41272d.png)

When we click the search button there are two scenarios that may happen on depending on the
Bluetooth status. These scenarios are shown below:
i. If the Bluetooth of the device is OFF, then a message will be displayed on the screen of
the device that askes for the Bluetooth permission. If we allow the permission then it
automatically continues to turn ON Bluetooth and shows a message saying, “Turning
Bluetooth ON” and after turning ON, it will then list the devices.

![image](https://user-images.githubusercontent.com/69731494/190862037-c3f34779-73d3-443d-b3e5-05fc6ef0a9f4.png)

This activity (interface) allows as to control to the robotic arm. As shown in the figure there are
six seek bars in the developed application. The figure shows them as they appear on the android
device. The name of each seek bars is written above them and their parts are tried to be depicted
on the next figure.

![image](https://user-images.githubusercontent.com/69731494/190862088-3bcb1f4e-a43b-4964-9cab-580d09e4e555.png)

Sliding each seek bar is a mechanism we have chosen to control the angle movements of the servo
motors in turn the arm structure. Additionally, if we want a repetition of movements then we can
save a step of positions by sliding the seek bars in different position and click the run button to
repeat. One thing to remember here is that saving of positions of the servo motor are done by
clicking the save button after each successive steps made. The task of saving the position of the
servo motors is accomplished by an array data structure defined in our code. This array stores the
snapshot of the position of the servos as soon as the save button is clicked.

![image](https://user-images.githubusercontent.com/69731494/190862107-f41f8517-f008-41d1-9f23-a2e8d9b4e472.png)



