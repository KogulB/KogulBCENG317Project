# CENG 317 PCF8591

The purpose of this project was to get a better understanding of the sensor I chose which was a PCF8591. I will use my sensor with my partners next semester as a collabaration project. I had to do some research on my sensor to learn about how much it would cost and what I needed to make it work with the Raspberry Pi. I put together a [Budget Plan](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Budget.xlsx) and a project Scehdule to help me utilize my porject in a successful manner.

## Introduction - System Diagram

![SystemDiagram](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/SystemDiagram.PNG)

## 2 Budget Plan/Bill

The main components of the project was an Rpi 3 Kit which included a power cable default case. Memory card would have to be purchased sepeartely but for myself I had my own already. More purchases made were the PCF8591, Jumper cables, Ethernet wire and adpater. HDMI cable and breadboard might need to be purchased as well but I previosuly own on already. There are however some extra parts purchased for testing but were never user used. The link to my budget plan can be found [here](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Budget.xlsx).

## 3 Time Commitment 

The time it took to do the research portion of my project took about two hours to find all the components needed to get my IC up and running.

The materials took about two days to ship and for me to get them. They were ordered from amazon. The PCF 8591 was however bought at the local Creatron store. 

After getting all the components hooking up the Rpi 3 to the senseor took around 3 hours. Toughest part of putting it together was figuring out where each part goes and how to connect it using a breadboard. I used a diagram from google to find out where each connector goes on the pcf8591 and also a diagram of Rpi 3 pin layout to figure where each connection is established. 

After figuring out the connection I spent about two hours creating the connection [diagram](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/BreadBoardLayout.PNG). This diagram gave me a version of a PCB. I spent another 5 hours designing and moving around the PCB diagram by adding Vias to it and making sure the connections didnt overlap. At the end this is how the PCB should look like([PCB](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/PCF8591PCB.PNG)).

This is a picture of the finished [PCB](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/PCBBoardSoldered.jpg) attached to my Rpi 3.

Creating the code for testing was not hard as all I had to do was pull the code from the StudentSenseHat Git. Since PCF8591 was used in that project Testing took about 30 minutes

### Total Commitment: 14 hours(excluding shipping)

## 4 PCB/Soldering


I had to cut off the pins located on the PCF8591 and solder header pins on both sides so I could connect it to my breadbaord. This was my first attempt at soldering so it was much more difficult.

I also had to solder new header pins on to my PCB so I could connect my Rpi and Sensor to the PCB. Soldering this time was easierbut involved more. 

## 5 Mechanical Assembly

Raspberry Pi 3: The Rpi 3 kit came with a power supply and case which made connection easier

PCF8591: Connect the PCF8591 to the Pins specified in my Diagram. Refer to this [diagram](https://github.com/KogulB/KogulBCENG317Project/blob/master/PCF8591PCBLayout/BreadBoardLayout.PNG). and [here](https://www.google.ca/url?sa=i&source=images&cd=&cad=rja&uact=8&ved=2ahUKEwii_Lrb1Y7fAhUp4oMKHcq3BWIQjRx6BAgBEAU&url=https%3A%2F%2Fwww.hackster.io%2Fthe-swiftpi-team%2Fswift-3-0-for-raspberry-pi-gpio-getting-started-393dd4&psig=AOvVaw19PAFSxnl2kqb4zXchUYGP&ust=1544304766474030) for the Rpi Pin layout.

VCC connects to Pin 2(5V)
GND connects to Pin 6(GND)
SDA connects to Pin 3(SDA1 I2C)
SCL connects to Pin 5 (SCL1 I2C)

Breadboard: When connecting to the breadboard I used ribbon cables provided with the board as well as jumper cables from my parts kit to connect the Rpi.

The diagram should look something like this when using a [breadboard](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/piSetupjpeg.jpeg).

The Enclosure for the Pi and PCB should look like [this](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/PiEnclosure.jpg).

## 6 Power Up

After making the connections a red indicator light on the Sensor should light up. Suggestion: connect the Rpi 3 GND pin first before connecting the power pin.

## 7 Production Testing

After powering the Rpi make sure you test if the address the 8591 is connected to is actually correct

#### Connnect Pi to a display using HDMI wire(or HDMI adapter)
#### Turn on the Pi (wait for it to boot up)
#### open a terminal window
#### run the command sudo raspi config
#### Enable I2C Address
#### Exit out
#### run sudo reboot
#### after reboot open another terminal window
#### run the command  sudo I2Cdetect -y 1
#### it should show that the address is 0x48

[Example](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/Assigned.PNG)

## 8 Unit Testing

#### run the command sudo git clone https://github.com/six0four/StudentSenseHat.git
#### This should clone the Student Sense Hat git to your root folder
#### run cd /StudentSenseHat/firmware
#### then run gcc -Wall -o traffic2B traffic2B.c -lwiringPi to compile the code
#### then to run the code sudo ./traffic2B

This should cause a green [light](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/LightSensor.jpg) to emit from the Pi. And the data being read should change the luminosity based on the light sensor on the PCF8591.

To test try covering the sensor with your hand to see what happens to the luminosity value(Light). 


