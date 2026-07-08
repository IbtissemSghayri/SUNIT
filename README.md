# SUNIT ESP32-based drone equiped with a camera

SUNIT is an intelligent drone-based inspection system designed to improve the monitoring and maintenance of solar photovoltaic installations.  
It is an esp32-based drone. It has a camera used to detect solar panals defects and help improve the efficiency of the panels by detecting overheat.
The design of the drone integrates a camera, a gps and an mpu-6050.  

# How does it work ?
The drone is equiped with a thermal camera that will scan the panals and connect in real time with a dashboard in order to analyse the panals data and detect defeated ones and the ones overheating, before the damage would happen.  
The drone is also equipped with a noamrl camera used to detect defects in the solar panals.  
The drone is monittored through a controller using esp32 which is connected to the drone through a transmitter-receiver module (RC communication)  

 # Components of the drone 
1 Chassis for the drone  
4 Brushless Motor  
4 Electronic Speed Controller (ESC) 30A  
1 MPU-6050  
1 PDB XT60  
1 LiPo Battery 2200mAh / 3s / 11.1 V  
1 GPS NEO 6M  
1 ESP32  
1 ESP32-CAM   [The idea was to use a thermal camera but we could not afford it so we used an ESP32-CAM for the prototype]

# Components of the controller


# Componants Testing 
The testing of the Brushless motors was done according to this scheme 
<img width="928" height="470" alt="image" src="https://github.com/user-attachments/assets/686b6336-3cdc-4aa5-b3c8-d96f34e0446e" />


# Wiring of the drone
Wiring of the drone : 
<img width="974" height="622" alt="image" src="https://github.com/user-attachments/assets/bfe10ea9-ff20-4b28-aee3-7b842af1917a" />

PDB XT60 is replaced with a DC-DC Step-Down Buck Converter Power Supply Module 24V 12V 9V to 5V 5A 25W  for the actual prototype in real-life as i did not find that component.

# Wiring of the controller

# Setbacks and mistakes
---> I thought that using 3 Lithium batteries 5V connected in series with a bms to give me stable 12V will give me enough energy to rotate the brushless.   That was not the case i figured that the Lipo batterie were not replaceable.   
Why ? becayse a 3S LiPo is built to deliver the burst current the A2212 motors need that the 3 separate cells wired in series (especially that mine are pulled from an old laptop) can not deliver enough current ! The answer is in current !
---> Some ESC are equipped with 2 extra thin wires I spent a lot of time checking the data sheet in order to understand that as i was used to the escs without these two, one is red the other is black. How to wire them ?   They are used to supply the controller of the esc's. You should connect them to 5V stable ! Using a DC-DC step-down buck converter would fix that. 

# Software used
Arduino.ide as the programming and development environment  
Fritzing and Cirkit designer  


# Reference 
https://docs.espressif.com/projects/espressif-esp-drone/en/latest/gettingstarted.html  
https://github.com/pratikPhadte/ESP32-Flight-controller-  
Article : Designing a Quadcopterfor Fire and Temperature Detection with an Infrared Camera and PIR Sensor Guruprasad Rathinakumar and Efstratios L. Ntantis *  
https://www.youtube.com/watch?v=BcPTe-hTJGc&list=PLo2ZwbR4rgURymVeGnCUaAI-kJ2RUVrf5  
https://www.ijert.org/precision-drone-control-using-mpu6050-sensor-integration
