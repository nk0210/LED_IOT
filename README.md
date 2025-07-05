# LED_IOT

# Smart LED Control using LDR and IR Sensor 🚦

This Arduino project turns an LED **ON** at night **only when** an object (like a vehicle or person) is detected nearby. It uses:
- An **LDR (Light Dependent Resistor)** to detect light levels.
- An **IR Sensor** to detect motion or presence.
- An **LED** as an indicator (e.g., street light or alert light).

## 🔧 Components Required

- Arduino Uno (or any compatible board)
- LDR Sensor
- IR Obstacle Sensor
- 10kΩ Resistor (for LDR voltage divider)
- LED
- Breadboard and jumper wires

## ⚙️ Circuit Connections

| Component      | Arduino Pin |
|----------------|-------------|
| LDR (via voltage divider) | A0          |
| IR Sensor OUT  | D2          |
| LED (+ve)      | D13         |

> Note: Connect GND and VCC (5V) properly for both sensors.

## 💡 Working Principle

- During **daylight** (`LDR value ≤ 600`), the LED stays **OFF**, regardless of object detection.
- During **darkness** (`LDR value > 600`), the LED turns **ON** **only when** the IR sensor detects a nearby object (IR output = LOW).

