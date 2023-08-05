# Electronics-and-Power-Department-Task-3
3rd task of Electronics and Power Department - Summer training program at Smart Methods

## Ultrasonic Sensor 
 A simple program that controls an Ultrasonic Sensor, which measures the distance between the device and an obstacle in front of it
 
 ### Tinkercad Link - Ultrasonic Sensor
 
https://www.tinkercad.com/things/fDtmolERbk6?sharecode=jRqQwBAYX5I4MR6WdLzFI3JS21C5UrVf_3hdqdfZpTk


![Ultrasonic Sensor - Task 3 ](https://github.com/H16Bw/Electronics-and-Power-Department-Task-3/assets/139852537/338bb844-8067-4318-90af-18d40c6cd9f7)


## Code 
The code uses three pins: 

- pin 3 as a digital output signal (OUTPUT).
- pin 4 to send a trigger pulse to the sensor (OUTPUT).
- and pin 5 to receive the digital signal from the sensor (INPUT).

### The main details of the code:

- ### setup():
   This function performs the initial configuration and is executed only once when the device starts up.

- ### loop():
  This function repeats continuously at a rate of approximately 16 times per second. It measures the distance using the sensor, outputs the result to the Serial Monitor, and sets the state of the signalPin based on the measured distance.

- ### pinMode():
  Used to set the mode of a specific pin, either OUTPUT or INPUT.

- ### digitalWrite():
  Used to set the state of a specific pin, either HIGH (1) or LOW (0).

- ### pulseIn():
  Used to measure the duration of a pulse on a specific pin. In this program, it measures the time taken by the sound wave to return to the sensor after hitting an obstacle.

The purpose of this code is to accurately measure the distance using the Ultrasonic Sensor. When the program is running, it sends a pulse from the trigPin to the sensor. When this pulse hits an obstacle and returns, the duration it takes for the sound to return is read through the echoPin. The distance is then calculated based on the measured duration and displayed on the Serial Monitor. Additionally, the signalPin is controlled based on the measured distance. If the distance is less than or equal to 50, the signalPin is set to HIGH. Otherwise, it is set to LOW. This digital signal control can be used to manage other systems based on the detected distance, such as triggering a warning signal or activating other devices.
