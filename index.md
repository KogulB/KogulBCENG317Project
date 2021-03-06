# [Kogul's CENG 317 Hardware Project](https://github.com/KogulB/KogulBCENG317Project)

### Week 13([Project Enclosure](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/myPiCasePCFRevision8.cdr))

#### November 27,2018
 This week I had to fix my Corel Draw design since my Enclosure did not fit my case due to dimension issues. This part of the project gave me some difficulty because I had very limited knowledge on CorelDraw and I am particularly weak when it comes to designing stuff through a program. After getting help from the proto type lab I was able to design my case successfully in a way that it could enclose my Rpi as well as my IC and PCB Board.

##### Updated Corel Draw Screenshot

![Updated CorelDraw](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/CORELDiagram.PNG)

##### Complelted Enclosure

![Enclosure](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/PiEnclosure.jpg)

### Week 12 ([Coral Diagram](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/myPiCasePCF.cdr))

#### November 20, 2018

Today in class I completed my design for the [Enclosure](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/myPiCasePCFRevision8.cdr) that is supposed to fit my Raspberry Pi as well as my IC and PCB Board. Starting this part of the project was a bit difficult for me as I have never used CorelDraw to design anything before. I used the resources from the Prototype Lab to successfully design the casing for my project. Since there was a wait time for the printing I was unable to acquire the parts. Will upload fully covered enclosure as soon as I put it together. Since I was able to finish the diagram today but not able to obtain my enclosure I am delayed according to my [project schedule](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Schedule.mpp). No further purchases were made this week so my [Budget](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Budget.xlsx) did not change.

##### Coral Draw Screenshot
![CorelDraw File](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/CORELDiagram.PNG)

### Week 11

#### November 13, 2018
Today I started the lab by attempting to connect to my Rpi through remote desktop but failed. I then signed out a cable to connect my pi to the computer directly and figure out the remote desktop problem later. By using the i2cdetect command I was able to double check sensor was connected to my pi. I was then told by the instructor that since StudentSenseHat project involved my pcf8591 sensor I could use that code to prove communication between the sensor and the platform development. Therefore, following the [instructions](https://github.com/six0four/StudentSenseHat#student-raspberry-pi-image-creation-and-test-code) I cloned the repository on to my Pi and then compiled and ran the code located inside the firmware folder. The compiled code than ran a greenhouse control system which shows different readings. The one that the pcf8591 is displaying is the readings from the light sensor which is located on the IC. Below are screenshots of what happens when there is exposure to light and what happens when I cover the sensor with my hands. As seen from the data when there is less exposure to light the higher the value is. This data proves successful communication between pi and IC. I will be editing and designing the acrylic case for the pi in the days to come to be ready for next week. I later came back to my earlier problem of connecting the pi remotely and discovered I could not connect at school. Since I was able to finish the testing today I am still on track with my [project schedule](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Schedule.mpp). No further purchases were made this week so my [Budget](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Budget.xlsx) did not change. 

##### Sensor Exposed to Room Light
![LightExposure](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/NotCovered.PNG)

##### Sensor Covered by Hand
![CoveredByHand](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/Covered.PNG)

##### Sensor Light
![Light](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/LightSensor.jpg)

### Week 10

#### November 6, 2018

##### Soldered Board
![SolderedBoard](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/PCBBoardSoldered.jpg)

##### Light up Sensor with PCB Board

![Rpi3SolderedBoard](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/Illumination.png)

Today in class I started working on soldering my PCB board to be able to attach it to the Rpi 3.
I ran into some trouble as I did not have any stackable header pins of my own but was able to find some extra ones in the Prototype Lab.
The soldering was a bit difficult for me as I did not have any prior experience doing it myself.
I had trouble figuring out what temperature to use to make sure the solder stuck.
My colleague and instructor were able to point me in the right direction and help me solder the board successfully.
After soldering I made sure everything was fine with my board by getting a second opinion as well as checking it under the microscope.
I was able to plug in my sensor to my board and my board to my development platform which in turn caused a light to illuminate on the sensor.
Further testing will be done by applying the I2cdetect command. As I have fully completed my soldering diagram today I am still on track with my [project schedule](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Schedule.mpp).
My [Budget Calculation](https://github.com/KogulB/KogulBCENG317Project/blob/master/documentation/Budget.xlsx) 
is still roughly the same as I was able to find the pins I needed in the Prototype Lab.

### Week 9

#### October 30, 2018

In class I worked on further developing my fritzing diagram so I was able to get a PCB printout.
I ran into some trouble with my diagram as it was not accurate enough to be able to create
a PCB board. Looking back at last years project Student Sense Hat I was able to reference my IC
as my PCF8591 was used in that project. With some help from the instructor I was able to figure out how to do the correct version of my fritzing diagram and complete my PCB layout successfully here are screenshots of my completed layout, breadboard and schematic:

![PCF8591ImagePCB](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/PCF8591PCB.PNG)

![PCF8591ImageBB](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/BreadBoardLayout.PNG)

![PCF8591ImageSch](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/PCF8591PCBLayout/PCF8591Schematic.PNG)


### Week 8
#### Oct 23, 2018

 Today in class I started doing some quick research on how to wire my PCF8591 to the 
 bread board so that it could connect to my Rpi 3. I attempted to connect my Rpi to the breadboard which had my IC mounted using alligator clippers. 
 After further explanation from my instructor I was told that using alligator clips could essentially damage my “pie” as the clips were too close together and touching. 
 I decided I was going to finish the rewiring at home with the proper wires that came with the chip. 
 My next step was to locate a Display adapter, so I could do a proper setup of NOOBs on the Rpi 3. 
 This was also not successful due to my file being corrupt, and I will be including a screenshot of the setup I created at home with works with proper functionality. 
 According to my schedule I created I am on time when it comes to completing the breadboard milestone but lagging on other items for the project such as PI setup. 
 I was able to successfully prove through the command I2cdetect that I am using the correct bus that I chose in the beginning of the term.


![PiSetup](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/piSetupjpeg.jpeg)

![PiSetup](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/PCF8591.png)

![PiSetup](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/PiScreen.jpeg)


![PiSetup](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/Images/Assigned.PNG)

##### Soldering my board
![Parts](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/CroppedSoldering.jpg)

#### Dual Color LED Proof of purchase

![Parts](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/documentation/Dual%20Color%20Led.jpg)
	
	
#### ADD To DA Converter Purchase  

![Parts](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/documentation/SunfounderADDApcf8591.PNG)

#### Rpi 3 and Usb 

![Parts](https://raw.githubusercontent.com/KogulB/KogulBCENG317Project/master/documentation/UsbandRpi3.PNG)

