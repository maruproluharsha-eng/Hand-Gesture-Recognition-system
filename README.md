AI-Based Hand Gesture Recognition System Using IMU Sensor and KNN

A real-time hand gesture recognition system that combines an MPU6050
IMU sensor, Arduino Uno, wireless communication, and the
K-Nearest Neighbors (KNN) machine learning algorithm to recognize
hand movements and enable gesture-based computer interaction.

📌 Overview

The system captures hand movement using the MPU6050's accelerometer and
gyroscope. The sensor is interfaced with an Arduino Uno, which collects
the motion data and sends it through a communication module.

The collected data is processed to extract useful motion features and is
classified using a KNN machine learning model. The recognized gesture
can then be mapped to a computer-control action such as mouse movement
or other predefined commands.

✨ Key Features

Real-time hand motion sensing using an MPU6050 IMU.

Accelerometer and gyroscope data acquisition.

Arduino-based embedded data collection.

Data preprocessing and feature extraction for gesture recognition.

KNN-based hand gesture classification.

Wireless communication between the embedded system and processing
system.

Gesture-based computer interaction.

Hardware prototype implementation.

🏗️ System Architecture

                    Hand Movement
                          |
                          v
                 +----------------+
                 |  MPU6050 IMU   |
                 | Accelerometer  |
                 | + Gyroscope    |
                 +-------+--------+
                         |
                         v
                 +----------------+
                 |   Arduino Uno  |
                 +-------+--------+
                         |
                         v
                 +----------------+
                 | Communication  |
                 |     Module     |
                 +-------+--------+
                         |
                         v
                 +----------------+
                 |     Feature    |
                 |   Extraction   |
                 +-------+--------+
                         |
                         v
                 +----------------+
                 | KNN Classifier |
                 +-------+--------+
                         |
                         v
                 +----------------+
                 | Gesture Output |
                 | / PC Control   |
                 +----------------+

🔧 Hardware Requirements

Component                           Purpose

Arduino Uno                         Microcontroller and sensor data
acquisition

MPU6050 IMU                         Accelerometer and gyroscope
measurements

Wireless Communication Module       Transfers data between the embedded
system and processing system

Jumper Wires                        Circuit connections

Battery / Power Source              Portable power supply

Prototype Board / Mounting Setup    Hardware implementation

💻 Software and Technologies

Python

Arduino IDE

K-Nearest Neighbors (KNN)

Machine Learning

Data Preprocessing

Feature Extraction

Serial Communication

I²C Communication

MPU6050 Sensor Interface

Add specific Python libraries to this section only if they were
actually used in the project.

📡 Sensor Data

The MPU6050 provides six motion measurements:

Accelerometer

Ax
Ay
Az

Gyroscope

Gx
Gy
Gz

These values describe the movement and orientation of the hand and form
the basis for gesture recognition.

Example sensor output:

Ax: 0.00 | Ay: 0.00 | Az: 1.00
Gx: 0.00 | Gy: 0.00 | Gz: 0.00
Gesture: IDLE

🔌 MPU6050 and Arduino Uno

The MPU6050 communicates with the Arduino Uno using the I²C
interface.

Typical Arduino Uno connections are:

MPU6050   Arduino Uno

VCC       Appropriate power supply for the breakout board
GND       GND
SDA       A4
SCL       A5

Check the voltage requirements of your specific MPU6050 breakout board
before making the power connection.

🤖 Machine Learning Workflow

1. Data Collection

Hand movements are performed while the MPU6050 records accelerometer and
gyroscope readings.

The collected samples are associated with gesture labels such as:

LEFT
RIGHT
UP
DOWN
IDLE

The exact gesture classes depend on the dataset used for training.

2. Data Preprocessing

The recorded sensor data is organized and prepared for machine learning.

Typical processing includes:

Removing invalid or unwanted readings.

Organizing sensor measurements.

Assigning gesture labels.

Preparing input features for classification.

3. Feature Extraction

Relevant motion information is extracted from the accelerometer and
gyroscope readings.

The resulting feature values are supplied to the KNN classifier.

4. KNN Classification

The K-Nearest Neighbors (KNN) algorithm classifies a new hand
movement by comparing its feature values with previously collected and
labeled samples.

Raw IMU Data
     |
     v
Data Preprocessing
     |
     v
Feature Extraction
     |
     v
KNN Classification
     |
     v
Recognized Gesture

🖱️ Gesture-Based Computer Interaction

After classification, a recognized gesture can be mapped to a computer
action.

For example:

Gesture   Possible Action

LEFT      Move cursor left
RIGHT     Move cursor right
UP        Move cursor up
DOWN      Move cursor down
IDLE      No action

The actual mapping depends on the implementation and trained gesture
classes.

🚀 Project Workflow

Assemble the MPU6050 and Arduino Uno hardware.

Establish I²C communication between the sensor and Arduino.

Read accelerometer and gyroscope values.

Transmit the collected sensor data through the communication module.

Collect and label gesture samples.

Preprocess the sensor dataset.

Extract relevant features.

Train the KNN classifier.

Test the classifier using new hand movements.

Map recognized gestures to computer-control actions.

📊 Expected Output

The system displays sensor measurements and the predicted gesture.

Example:

Ax: 0.32 | Ay: -0.14 | Az: 0.91
Gx: 12.40 | Gy: -5.20 | Gz: 3.10
Gesture: RIGHT

🎯 Applications

Human-Computer Interaction (HCI)

Touchless computer control

Gesture-controlled interfaces

Assistive technology

Wearable devices

Robotics and embedded systems

Smart device control

🔮 Future Improvements

Increase the number of supported gestures.

Improve recognition accuracy with a larger and more diverse dataset.

Apply sensor-noise filtering and calibration.

Compare KNN with other machine learning algorithms.

Develop a compact wearable PCB.

Improve wireless communication reliability.

Add more computer-control functions.

Optimize the system for lower latency and real-time operation.

🧰 Skills Demonstrated

Embedded Systems · Machine Learning · Python · Arduino · MPU6050 · KNN
· IMU Sensors · Accelerometer · Gyroscope · Data Preprocessing · Feature
Extraction · I²C Communication · Serial Communication · Human-Computer
Interaction

👨‍💻 Project Type

Academic Project

📄 Project Summary

Developed an AI-based hand gesture recognition system using an MPU6050
IMU sensor and Arduino Uno. The system collects accelerometer and
gyroscope data, performs data preprocessing and feature extraction, and
uses the KNN algorithm to classify hand gestures. Wireless communication
enables the recognized gestures to be used for computer interaction,
demonstrating the integration of machine learning with embedded systems.
