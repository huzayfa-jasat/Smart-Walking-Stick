# Smart-Walking-Stick
An assistive device that uses ultrasonic sensors to detect obstacles and provides real-time feedback through vibrations or sound alerts.

## **How It Works**<br/><br/>
### **Overview**<br/>
The Smart Detecting Walking Stick enhances mobility for visually impaired users by detecting nearby obstacles and providing haptic or auditory feedback. It uses three ultrasonic sensors to measure distances and a buzzer to signal detected obstacles.<br/>

### Hardware Components
Ultrasonic Sensors (HC-SR04) – Detects obstacles in three directions (front, left, right).<br/>
Buzzer – Provides audio feedback based on obstacle proximity.<br/>
Arduino Board – Processes sensor data and controls output signals.<br/>
Power Source – Typically a rechargeable battery or USB power supply.<br/>

### Optimization Process<br/>
#### 1. Distance Measurement<br/>
The ultrasonic sensors send out pulses and measure the time it takes for the echo to return.<br/>
Distance is calculated using the formula: (Time * Speed)/2<br/>
 
#### 2. Obstacle Detection & Alert System
If an obstacle is detected within 100 cm, the buzzer emits a tone.<br/>
Different frequencies indicate different directions:<br/>
500 Hz – Front obstacle<br/>
700 Hz – Left/Right obstacle<br/>
If no obstacles are detected, the buzzer remains silent.<br/>

### Code Implementation
File: motion_detecting_walking_stick.ino<br/>
#### Key Functionalities:<br/>
• Ultrasonic Sensing – Measures distance using three sensors.<br/>
• Obstacle Alerts – Activates a buzzer when objects are too close.<br/>
• Directional Feedback – Different tones help users identify obstacle direction.<br/>
• Efficient Loop Execution – Optimized for minimal delay and continuous operation.<br/>

### Performance & Accuracy<br/>
The system effectively detects obstacles up to 100 cm and provides immediate feedback with minimal delay.<br/>

### Test Results:<br/>
| Scenario | Detection Distance | Buzzer Response |
| :---         |     :---:      |          ---: |
| No obstacles   | > 100 cm     | No tone    |
| Obstacle in front  |	< 100 cm  |500 Hz tone  |
| Obstacle on left  | < 100 cm	| 700 Hz tone|
|Obstacle on right	|< 100 cm	|700 Hz tone|<br/>

### Potential Improvements<br/>
• Vibration Feedback – Add a vibration motor for silent alerts.<br/>
• AI Integration – Use AI to predict movement patterns and adjust alerts.<br/>
• Bluetooth Connectivity – Integrate with a mobile app for additional accessibility features.<br/>
• Battery Optimization – Implement power-saving modes for extended use.<br/>

### References<br/>
Arduino Docs: https://www.arduino.cc/<br/>
HC-SR04 Datasheet: https://components101.com/ultrasonic-sensor-working<br/>
PulseIn Function: https://www.arduino.cc/reference/en/language/functions/time/pulsein/
