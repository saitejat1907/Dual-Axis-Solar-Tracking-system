# Solar Tracking System Using Arduino

## Project Overview
The **Solar Tracking System** is designed to maximize the efficiency of solar panels by ensuring they are always aligned with the direction of maximum sunlight. Using photoresistors, an Arduino microcontroller, and servo motors, the system dynamically rotates the solar panels to follow the path of the sun throughout the day, thereby increasing the overall energy output of the panels.

## Features
- **Automated Sun Tracking**: The system rotates the solar panels towards the direction of maximum sunlight using 4 photoresistors mounted on the sides of the solar panel.
- **Increased Efficiency**: By dynamically adjusting the panel’s orientation, this system can increase power generation by 30% to 60% compared to a fixed-position solar panel.
- **Arduino Controlled**: The system is powered by an Arduino microcontroller running a custom C code that processes data from the photoresistors and controls the motors.

## Detailed Documentation
For a comprehensive overview of the project, including results, introduction, and all related information, please refer to the detailed documentation: [Solar Tracking System Documentation](https://github.com/saitejat1907/Dual-Axis-Solar-Tracking-system/blob/main/Mini%20Project%20Final%20report.pdf)


## Images

### 1. Functionality Overview
This image shows the general functionality of how the solar panel tracks sunlight.
![Functionality Overview](https://github.com/saitejat1907/Dual-Axis-Solar-Tracking-system/blob/main/picture1.jpg)

### 2. Circuit Connection
Here is the schematic of the circuit connections used in the project.
![Circuit Connection](https://github.com/saitejat1907/Dual-Axis-Solar-Tracking-system/blob/main/picture2.jpg)

### 3. Prototype
This is the prototype we built, demonstrating the solar tracking system in action.
![Prototype](https://github.com/saitejat1907/Dual-Axis-Solar-Tracking-system/blob/main/picture3.jpg)

## Project Components
- **Solar Panel**: Captures sunlight and converts it to electrical energy.
- **Arduino Microcontroller**: The brain of the system that processes input from the photoresistors and controls the servo motors.
- **Photoresistors (LDR)**: Light-dependent resistors detect the intensity of sunlight from different directions.
- **Servo Motors**: Responsible for rotating the solar panel towards the direction with the highest sunlight intensity.
- **C Programming Language**: The code deployed on the Arduino to execute the logic for tracking the sunlight.

## How It Works
1. The photoresistors sense the intensity of sunlight from four directions.
2. The Arduino processes the sensor data and determines the direction with the highest light intensity.
3. Based on the sensor input, the Arduino sends signals to the servo motors to rotate the solar panel in the optimal direction.
4. The panel follows the sun’s movement throughout the day, ensuring maximum power absorption.

## Benefits of Solar Tracking
- **Increased Power Output**: By adjusting to the sun’s position, this system ensures the solar panel is always in the most efficient position, increasing power output by up to 60%.
- **Simple and Cost-Effective**: The system is designed using readily available components and offers a cost-effective solution for improving solar panel efficiency.

## Project Setup

### Hardware Setup:
- Connect the solar panel to the Arduino.
- Attach the 4 photoresistors to the sides of the solar panel.
- Connect the servo motors to the Arduino for controlling the panel’s rotation.

### Software Setup:
- Write and deploy the C code to the Arduino.
- The code controls the logic for reading the photoresistor values and sending rotation commands to the servo motors.

### Execution:
- Power on the Arduino and let the system automatically track the sun’s movement.
- Observe the solar panel rotate throughout the day to follow the sun and maximize energy generation.

## Code Example
Below is a simplified snippet of the logic in C for controlling the Arduino:

```c
int ldrLeft = A0; // Left photoresistor
int ldrRight = A1; // Right photoresistor
int ldrTop = A2; // Top photoresistor
int ldrBottom = A3; // Bottom photoresistor
int motorPin = 9; // Servo motor pin

void setup() {
  pinMode(motorPin, OUTPUT);
}

void loop() {
  int leftValue = analogRead(ldrLeft);
  int rightValue = analogRead(ldrRight);
  
  // Compare light intensities and rotate panel
  if (leftValue > rightValue) {
    // Rotate towards the left
  } else {
    // Rotate towards the right
  }
}
```
