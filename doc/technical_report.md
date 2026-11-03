
# USB-C LiDAR Node (VL53L9)
### Technical Overview & Capabilities Report

## 1. Board Overview

### 1.1 Project Purpose


### 1.1 Project Purpose

The USB-C LiDAR Node is a compact, low-cost sensing board designed to combine 3D distance measurements with motion data.

It integrates a VL53L9CX LiDAR sensor and an LSM6DSV 6-axis Inertial Measurement Unit (IMU). An STM32 microcontroller is intended to collect the sensor data and transmit it to a host computer via USB-C.

The LiDAR sensor provides spatial distance information, while the IMU measures acceleration and angular velocity. Combining these measurements can help interpret the surrounding environment while the board is moving, making the system useful for robotics and navigation applications.

Potential applications include mobile robotics, small drones, and Simultaneous Localization and Mapping (SLAM) research.


### 1.2 System Architecture

The board consists of two sensors, an STM32 microcontroller, a USB-C interface, and an integrated power supply circuit.

#### System Block Diagram

![System Block Diagram](block_diagram.png)

#### Data Flow

The VL53L9CX measures distances, while the LSM6DSV provides acceleration and angular velocity measurements.

Both sensors are connected to the STM32 microcontroller, which is intended to collect and process their data before transmitting it to a host computer through USB Full-Speed.

According to the schematic, the LiDAR uses SDA/SCL communication signals, while the IMU is connected through an SPI interface.

#### Power Supply

The board is designed to receive 5 V through its USB-C connector.

The power regulation circuit generates the required voltage rails, including 3.3 V, 2.8 V, 1.8 V, and 1.2 V, to supply the different components.

**Sources:**
- [Project README](../README.md)
- [MCU Schematic](../pcb/MCU.kicad_sch)
- [LiDAR Schematic](../pcb/lidar.kicad_sch)
- [IMU Schematic](../pcb/IMU.kicad_sch)
- [Power Schematic](../pcb/power.kicad_sch)


