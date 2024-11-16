# 🚗 **Car Parking System** 🚗

Welcome to the **Car Parking System** project! This system leverages embedded systems to automate and manage vehicle entry and exit in a parking lot. It utilizes sensors, a servo motor, and Bluetooth communication to create an intelligent and efficient parking management solution.

## 📦 **Items Used** 

- **Tx (Transmitter)**: For wireless communication.
- **Rx (Receiver)**: To receive signals from the transmitter.
- **IR1 (PA0 - Entry Sensor)**: Infrared sensor for vehicle entry detection.
- **IR2 (PA1 - Exit Sensor)**: Infrared sensor for vehicle exit detection.
- **Servo Motor**: To control the parking barrier (open/close functionality).
- **Bluetooth Module (PA2, PA3)**: Used to control and monitor the system via Bluetooth-enabled devices.

## 🛠️ **Hardware Connections** 

1. **IR Sensors**:
   - **IR1 (PA0)**: Detects vehicle entry.
   - **IR2 (PA1)**: Detects vehicle exit.

2. **Bluetooth Module**:
   - **TX Pin**: PA2
   - **RX Pin**: PA3

3. **Servo Motor**:
   - Connect the servo motor signal pin to an available GPIO pin.
   - VCC to power supply and ground to the common ground.

4. **Transmitter and Receiver**:
   - Used for additional communication functionality.

## ⚙️ **How It Works** 

1. **Vehicle Entry**: 
   - When a car approaches, the **IR1 sensor (PA0)** is activated, triggering the **servo motor** to open the parking gate. 
   - The system keeps track of available parking slots to avoid overflow.

2. **Vehicle Exit**:
   - When a vehicle exits, the **IR2 sensor (PA1)** is triggered, and the system closes the parking gate after the vehicle has left.
   
3. **Bluetooth Communication**:
   - The system can be monitored and controlled remotely via Bluetooth (PA2 and PA3).
   - **Bluetooth control** allows users to check parking slot availability or manually open/close the gate via their smartphone or Bluetooth-enabled devices.

## 💻 **Software Overview** 

- The software runs on a microcontroller (e.g., STM32), handling:
  - **Sensor input**
  - **Motor control** 
  - **Bluetooth communication** 

- The microcontroller uses **UART** for communication with the Bluetooth module.
- The system includes logic to handle vehicle entry/exit, ensuring the servo motor operates only when the corresponding sensor is triggered.

## 📹 **View Video for Reference**

For a better understanding of how the system works in real-time, [watch this demo video](#) demonstrating the complete functionality of the Car Parking System.

---

## ⚡ **Future Enhancements** 

- Integration with cloud systems for remote monitoring and reporting.
- Use of **Wi-Fi** for advanced communication features.
- Addition of **more sensors** for greater accuracy and reliability.

---

## 📝 **Setup Guide**

### Hardware Setup:
1. Connect the components as per the connections mentioned above.
2. Ensure the microcontroller is powered and connected to the required peripherals (IR sensors, Bluetooth, servo motor).

### Software Setup:
1. Upload the embedded code to the microcontroller using an IDE like **STM32CubeIDE** or **Keil**.
2. Compile the code and ensure there are no errors.
3. Test the system by simulating vehicle entry and exit events.
4. Use the Bluetooth connection to monitor and control the system from your phone or Bluetooth device.

---

## 🔒 **License** 

This project is **not open-source**. All rights to the code and design are reserved.

---

