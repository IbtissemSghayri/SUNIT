# SUNIT ESP32-based drone equiped with a camera
SUNIT is an intelligent drone-based inspection system designed to improve the monitoring and maintenance of solar photovoltaic installations.
It is an esp32-based drone. It has a camera used to detect solar panals defects and help improve the efficiency of the panels by detecting overheat.
The design of the drone integrates a camera, a gps and an mpu-6050.

# Componants Testing 
The testing of the Brushless motors was done according to this scheme 
<img width="928" height="470" alt="image" src="https://github.com/user-attachments/assets/686b6336-3cdc-4aa5-b3c8-d96f34e0446e" />


# Wiring 
Wiring of the drone : 
<img width="974" height="622" alt="image" src="https://github.com/user-attachments/assets/bfe10ea9-ff20-4b28-aee3-7b842af1917a" />

PDB XT60 is replaced with a DC-DC Step-Down Buck Converter Power Supply Module 24V 12V 9V to 5V 5A 25W in real-life as i did not find that component.




# Setbacks and mistakes
---> I thought that using 3 Lithium batteries 5V each will give me enough energy to rotate the brushless. That was not the case i figured that the Lipo batterie were not replaceable


# Software used
Arduino.ide as the programming and development environment
Fritzing and Cirkit designer


# Reference 
https://docs.espressif.com/projects/espressif-esp-drone/en/latest/gettingstarted.html
https://github.com/pratikPhadte/ESP32-Flight-controller-
Article : Designing a Quadcopterfor Fire and Temperature Detection with an Infrared Camera and PIR Sensor Guruprasad Rathinakumar and Efstratios L. Ntantis *
https://www.youtube.com/watch?v=BcPTe-hTJGc&list=PLo2ZwbR4rgURymVeGnCUaAI-kJ2RUVrf5
https://www.ijert.org/precision-drone-control-using-mpu6050-sensor-integration
