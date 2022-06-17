# Experiemnt--09-Line follower Robot
  

## AIM: 
To Design a line follower robot and control its motion using differential velocity 
 
### COMPONENTS REQUIRED:
 Arduino Uno - 1Nos
L293D motor driver- 1Nos
IR sensor module -2 Nos
7.4 or 9V battery -1 Nos
BO motor - 2 Nos
Motor wheel - 2 Nos
Castor wheel - 1 Nos
Hobby robot chassis - 1 Nos
Wires
Screw


### THEORY: 

 Line Follower Robot (LFR) is a simple autonomously guided robot that follows a line drawn on the ground to either detect a dark line on a white surface or a white line on a dark.
Working of a Line Follower Robot
As stated earlier, line follower robot (LFR) follows a line, and in order to follow a line, robot must detect the line first. Now the question is how to implement the line sensing mechanism in a LFR. We all know that the reflection of light on the white surface is maximum and minimum on the black surface because the black surface absorbs maximum amount of light. So, we are going to use this property of light to detect the line. To detect light, either LDR (light-dependent resistor) or an IR sensor can be used. For this project, we are going with the IR sensor because of its higher accuracy. To detect the line, we place two IR sensors one on the left and other on the right side of the robot as marked in the diagram below. We then place the robot on the line such that the line lies in the middle of both sensors. We have covered a detailed Arduino IR sensor tutorial which you can check to learn more about the working of IR sensors with Arduino Uno.

Infrared sensors consist of two elements, a transmitter and a receiver. The transmitter is basically an IR LED, which produces the signal and the IR receiver is a photodiode, which senses the signal produced by the transmitter. The IR sensors emits the infrared light on an object, the light hitting the black part gets absorbed thus giving a low output but the light hitting the white part reflects back to the transmitter which is then detected by the infrared receiver, thereby giving an analog output. Using the stated principle, we control the movement of the robot by driving the wheels attached to the motors, the motors are controlled by a microcontroller.

How does a Line Follower Robot Navigates?
A typical line follower robot has two sets of motors, let's call them left motor and right motor. Both motors rotate  on the basis of the signal received from the left and the right sensors respectively. The robot needs to perform 4 sets of motion which includes moving forward, turning left, turning right and coming to a halt. The description about the cases are given below.


Moving Forward:

![image](https://user-images.githubusercontent.com/36288975/174259113-a3c52236-17cb-48a8-afad-89557bef5477.png)


In this case, when both the sensors are on a white surface and the line is between the two sensors, the robot should move forward, i.e., both the motors should rotate such that the robot moves in forward direction (actually both the motors should rotate in the opposite direction due to the placement of motors in our setup. But for the sake of simplicity, we will call the motors rotating forward.)

Turning LEFT:
![image](https://user-images.githubusercontent.com/36288975/174259147-883ed76f-a39e-4567-864d-382c719db0c6.png)
In this case, the left sensor is on top of the dark line, whereas the right sensor is on the white part, hence the left sensor detects the black line and gives a signal, to the microcontroller. Since, signal comes from the left sensor, the robot should turn to the left direction. Therefore, the left motor rotates backwards and the right motor rotates in forward direction. Thus, the robot turns towards left side.

Turning RIGHT:
![image](https://user-images.githubusercontent.com/36288975/174259209-31089d55-5c87-4b40-8a7d-aa0600c95ddc.png)


This case is similar to the left case, but in this situation only the right sensor detects the line which means that the robot should turn in the right direction. To turn the robot towards the right direction, the left motor rotates forward and the right motor rotates backwards and as a result, the robot turns towards the right direction.

Stopping:
![image](https://user-images.githubusercontent.com/36288975/174259247-aac8e057-8c8c-41e6-bbcb-ec99b4c6d3b5.png)



### Circuit diagram 

![Line-Follower-Circuit-Diagram](https://user-images.githubusercontent.com/36288975/174259316-3af25033-ecff-4962-b953-6fe85c13c62f.png)
The circuit consists of mainly four parts: Two IR sensors, one motor drive, two motors, one Arduino, a battery and few connecting wires. The sensor senses the IR light reflected from the surface and feeds the output to the onboard op-amp comparator. When the sensor is situated over the white background, the light emitted by the sensor is reflected by the white ground and is received by the receiver. But when the sensor is above the black background, the light from the source doesn’t reflect to it. The sensor senses the intensity of reflected light to give an output. The sensor’s output is fed to the microcontroller, which gives commands to the motor driver to drive the motor accordingly. In our project, the Arduino Uno is programmed to make the robot move forward, turn right or turn left and stop according to the input coming from the sensor. The output of the Arduino is fed to the motor driver.


### PROCEDURE:
1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select the board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 
10.	Plot the graph for the output voltage vs the resistance 


### PROGRAM 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

 
 














### RESULTS : 
### WORKING VIDEO  :




