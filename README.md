# Power Loom Color Box Automation

## Overview

The **Power Loom Color Box Automation** system is designed to automate the color box switching in a power loom for the textile industry. This project aims to change the color thread boxes automatically based on user input and machine parameters. The system is based on the **PIC18F4550 microcontroller** and utilizes a **24C128 EEPROM** for data storage, along with **proximity sensors** for thread counting. The color change mechanism is controlled by a **DC solenoid** activated via a **MOSFET**, and the machine settings are displayed on a **20x4 LCD**. This project integrates seamlessly into textile machines, ensuring smooth operation for creating multicolor fabrics like sarees.

# Power Loom Color Box Automation

## Images Overview

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_1.jpg" alt="COLOR_BOX_1" width="150">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_2.jpg" alt="COLOR_BOX_2" width="150">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_3.jpg" alt="COLOR_BOX_3" width="150">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_4.jpg" alt="COLOR_BOX_4" width="150">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_5.jpg" alt="COLOR_BOX_5" width="150">
  <img src="https://github.com/karthirilla/Power_Loom_Color_Box_Automation/blob/main/COLOR_BOX_6.jpg" alt="COLOR_BOX_6" width="150">
</div>


### Key Features

- **Microcontroller**: Uses **PIC18F4550** for controlling the entire system, including managing input data, counting threads, and activating the solenoid.
- **Weft Thread Counting**: Monitors thread count using **proximity sensors**.
- **Color Box Switching**: Automatically changes the color box using a **DC solenoid** controlled by **MOSFET** to position the correct box based on user input.
- **User Interface**: The system provides a **20x4 LCD** display for showing machine data, settings, and current status.
- **Data Storage**: **24C128 EEPROM** is used to store the user settings and color box configurations.
- **Automation**: The system automates the color change based on a **4x4 matrix input**, ensuring accurate color matching for the fabric.
- **Industrial Integration**: Designed for seamless integration with textile machines, providing reliability and flexibility.

## System Components

- **Microcontroller**: **PIC18F4550** for managing inputs, outputs, and overall system control.
- **Sensors**: 
  - **Proximity Sensors**: Used to count the threads (weft) in the loom.
- **Actuators**: 
  - **DC Solenoid**: Controls the switching mechanism of the color box.
  - **MOSFET Driver**: Controls the DC solenoid for precise box movement.
- **Display**: 
  - **20x4 LCD**: Displays user inputs, current settings, and status information.
- **Memory**: 
  - **24C128 EEPROM**: Stores color box configurations, user settings, and other relevant data.
- **Power Supply**: Power system for the microcontroller, sensors, relays, and solenoid.

## Features in Detail

### 1. **Weft Thread Counting**
The system uses **proximity sensors** to detect the passage of the weft threads through the loom. It counts the threads to ensure the correct number of threads are used and triggers color changes when needed. This thread count is displayed on the **20x4 LCD** for user monitoring.

### 2. **Automatic Color Box Switching**
Once the user enters the required configuration (such as the desired number of threads for each color), the system automatically switches the color thread box at the right moment. This is achieved by activating the **DC solenoid** via the **MOSFET**, which positions the color box accordingly.

### 3. **User Interface**
The **20x4 LCD** serves as the user interface where operators can:
- Input settings via buttons or switches.
- View real-time data, such as thread count and box switching status.
- Adjust settings such as thread count, color assignments, and other parameters.
  
A **4x4 matrix keypad** can be used to input the settings and configurations for each color change cycle.

### 4. **Data Storage**
User configurations, including thread count, color assignments, and other parameters, are stored in the **24C128 EEPROM**. This ensures that settings are preserved even when the system is powered off.

### 5. **Automation Logic**
The automation flow is designed to:
- Automatically count the threads using the proximity sensor.
- Trigger the correct color box change using the solenoid based on preset configurations.
- Display all relevant machine data on the LCD, allowing for real-time monitoring of the automation process.

---

## System Workflow

1. **Startup**: On system initialization, the **PIC18F4550** reads stored settings from the **24C128 EEPROM** and displays them on the **20x4 LCD**.
2. **User Input**: The user enters the configuration settings via the **4x4 matrix keypad**, which could include the number of threads per color box, desired color sequence, etc.
3. **Thread Counting**: As the loom operates, **proximity sensors** detect the passage of the weft threads and count them. The system checks the number of threads and triggers a color box change when necessary.
4. **Color Box Change**: When the required number of threads is reached, the system activates the **DC solenoid** using the **MOSFET**, which moves the appropriate color box into place.
5. **Display Updates**: The **20x4 LCD** continuously updates with the current settings, thread count, and color box change status.
6. **Data Storage**: Settings and configurations are periodically saved to the **24C128 EEPROM**, ensuring data persistence.

---

## Circuit Diagram

The system's circuit diagram will illustrate the following:
- **PIC18F4550** connections to **proximity sensors**, **LCD**, and **4x4 matrix keypad**.
- **DC solenoid** controlled by a **MOSFET**.
- Connections for **24C128 EEPROM** to store user configurations.
- **Power isolation** techniques for safe operation with industrial machinery.

---

## Hardware Components List

1. **PIC18F4550 Microcontroller**
2. **24C128 EEPROM**
3. **Proximity Sensors** (for thread counting)
4. **DC Solenoid** (for color box switching)
5. **MOSFET Driver** (for controlling the solenoid)
6. **20x4 LCD Display**
7. **4x4 Matrix Keypad**
8. **Push Buttons** (for manual inputs like start, stop, reset)
9. **Power Supply Components** (for microcontroller, sensors, solenoid, etc.)

---

## Software and Development Environment

- **MPLAB IDE**: Used for coding and debugging the project.
- **XC8 Compiler**: Compiler for generating machine code for the PIC18F4550 microcontroller.
- **microC**: Alternative software tool for certain functionalities if needed.
- **CCS Compiler**: For ease of integration with peripherals.

---

## Contributing

Feel free to fork the repository, report bugs, and submit pull requests. Contributions to improve the functionality and stability of the project are welcome.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Thanks to the **MPLAB IDE**, **CCS Compiler**, and **microC** for their powerful tools that made this project possible.
- Special thanks to the contributors and the open-source community for their valuable support.

