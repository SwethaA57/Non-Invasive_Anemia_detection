# Non-Invasive Anemia Detector

## Overview

This project explores the feasibility of estimating hemoglobin concentration non-invasively using optical sensing techniques. The system uses a MAX30102 sensor to acquire red and infrared photoplethysmography (PPG) signals from a fingertip and processes the data on an ESP32 microcontroller to estimate hemoglobin levels.

The project was developed as a mini project under the Department of Electronics Engineering, Saintgits College of Engineering (Autonomous).

## Motivation

Conventional anemia diagnosis relies on laboratory blood tests, which are invasive and require specialized infrastructure. The objective of this work was to develop a low-cost proof-of-concept system capable of providing preliminary hemoglobin estimation using readily available embedded hardware.

## Hardware Used

* ESP32 DevKit V1
* MAX30102 Pulse Oximeter and Heart Rate Sensor
* SSD1306 OLED Display
* Push Button
* Breadboard and jumper wires

## System Architecture

The system consists of three main stages:

1. Signal Acquisition

   * Red and infrared signals are acquired using the MAX30102 sensor.

2. Signal Processing

   * Multiple samples are collected over a fixed interval.
   * Signal averaging and filtering are applied to reduce noise.
   * The ratio between red and infrared components is computed.

3. Hemoglobin Estimation

   * A regression-based calibration equation is used to estimate hemoglobin concentration.
   * The estimated value is classified and displayed on an OLED screen.

## Working Principle

The system is based on the Beer–Lambert principle, where light absorption depends on the concentration of an absorbing substance.

Red (660 nm) and infrared (940 nm) light are transmitted through the fingertip. Since hemoglobin exhibits wavelength-dependent absorption characteristics, the reflected optical signals can be processed to derive features related to hemoglobin concentration.

The estimated hemoglobin value is obtained using a calibration model developed from experimental observations.

## Features

* Non-invasive measurement approach
* Real-time hemoglobin estimation
* OLED-based user interface
* Portable embedded implementation
* Low hardware cost
* Simple one-button operation

## Project Cost

| Component       | Cost (INR) |
| --------------- | ---------- |
| ESP32 DevKit V1 | 415        |
| MAX30102        | 245        |
| OLED Display    | 330        |
| Breadboard      | 80         |
| Jumper Wires    | 50         |
| Total           | 1120       |

## Results

The prototype successfully acquired optical signals from the fingertip, estimated hemoglobin values using the implemented calibration model, and displayed the corresponding classification on the OLED display.

Testing showed consistent operation under controlled measurement conditions. The project demonstrates the potential of low-cost optical sensing for preliminary anemia screening.


## Future Work

* Clinical calibration using larger datasets
* Machine learning-based prediction models
* Skin-tone adaptive calibration
* Wireless data logging
* Mobile application integration
* Wearable implementation

## Disclaimer

This project is intended for educational and research purposes only. The device is not designed or validated for clinical diagnosis and should not be used as a substitute for professional medical testing.

## Contributors

Britty Siby,
Devika S,
Devika S Nair,
Swetha Anil,

Department of Electronics Engineering
Saintgits College of Engineering (Autonomous)
