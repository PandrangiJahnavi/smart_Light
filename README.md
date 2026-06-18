# Smart Ambient Light Monitoring System using ESP32 and BH1750

## Overview

This project uses an ESP32 microcontroller and a BH1750 Digital Light Sensor to measure ambient light intensity in lux (lx). Based on the detected light level, the system automatically controls two LEDs to simulate intelligent lighting behavior.

The system adjusts the number of LEDs turned ON according to environmental brightness conditions, demonstrating an energy-efficient smart lighting solution.

## Features

* Real-time light intensity monitoring
* Automatic LED control
* Digital light measurement in Lux (lx)
* Energy-efficient lighting logic
* I2C communication with BH1750
* Serial Monitor status display

## Components Required

* ESP32 Development Board
* BH1750 Light Sensor Module
* 2 LEDs
* 220Ω Resistors
* Breadboard
* Jumper Wires

## Pin Connections

### BH1750 Sensor

| BH1750 | ESP32   |
| ------ | ------- |
| VCC    | 3.3V    |
| GND    | GND     |
| SDA    | GPIO 21 |
| SCL    | GPIO 22 |

### LEDs

| LED   | ESP32 Pin |
| ----- | --------- |
| LED 1 | GPIO 23   |
| LED 2 | GPIO 13   |

## Working Principle

1. The BH1750 measures ambient light intensity.
2. The ESP32 reads the lux value through I2C communication.
3. Depending on the brightness level, LEDs are controlled automatically.
4. The current lux value and lighting condition are displayed on the Serial Monitor.

## Lighting Logic

| Light Intensity (Lux) | LED Status        | Condition      |
| --------------------- | ----------------- | -------------- |
| < 10 lx               | LED1 ON + LED2 ON | Dark           |
| 10 - 100 lx           | LED2 ON           | Dim            |
| 100 - 500 lx          | LED1 ON           | Moderate Light |
| > 500 lx              | Both LEDs OFF     | Bright         |

## Serial Monitor Output

### Dark Environment

```text
Light: 5.00 lx => Dark, TWO LEDs ON
```

### Dim Environment

```text
Light: 50.00 lx => Dim, ONE LED ON
```

### Moderate Light

```text
Light: 250.00 lx => Light, ONE LED ON
```

### Bright Environment

```text
Light: 800.00 lx => Bright, TWO LEDs OFF
```

## Applications

* Smart Home Lighting
* Energy Saving Systems
* Automatic Room Lighting
* Building Automation
* Industrial Light Monitoring
* Smart City Projects

## Technologies Used

* ESP32
* BH1750 Digital Light Sensor
* Arduino IDE
* I2C Communication
* Embedded C/C++

## Future Enhancements

* PWM Brightness Control
* OLED Display Integration
* Blynk IoT Dashboard
* ThingSpeak Cloud Monitoring
* Motion Sensor Integration
* Smart Street Lighting System

## Project Level

### Level 1

Light intensity monitoring using BH1750.

### Level 2

Automatic lighting control.

### Level 3

Energy-efficient smart lighting system.

#OUTPUT

https://github.com/PandrangiJahnavi/smart_Light/blob/main/Screenshot%202026-06-16%20094525.png
https://github.com/PandrangiJahnavi/smart_Light/blob/main/WhatsApp%20Image%202026-06-18%20at%2011.11.28%20AM.jpeg
https://github.com/PandrangiJahnavi/smart_Light/blob/main/WhatsApp%20Image%202026-06-18%20at%2011.11.29%20AM.jpeg
https://github.com/PandrangiJahnavi/smart_Light/blob/main/WhatsApp%20Image%202026-06-18%20at%2011.11.29%20AM.jpeg

## Author

**Pandrangi Jahnavi**

B.E. Electronics and Communication Engineering (ECE)

AWS Certified Cloud Practitioner

IoT | Embedded Systems | Smart Lighting | Industrial IoT
