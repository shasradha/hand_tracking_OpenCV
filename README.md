# hand_tracking_OpenCV
Make project with Ardunio and Python (OpenCV)

-------------------------------------------------------------------

# Arduino Hand Tracking Controller

This repository contains the code to control an Arduino-based system using hand tracking. The application is built with Python and requires Python version 3.10.0 to function correctly. Below are the instructions to set up and run the project.

---

## Prerequisites

### **Python Version**
- This project works only with **Python 3.10.0**.
- Download Python 3.10.0 from the official [Python website](https://www.python.org/downloads/release/python-3100/).

### **Required Libraries**
Install the following Python libraries:
- `pyfirmata` (For communication with Arduino)
- `opencv-python` (For image processing)
- `cvzone` (For hand tracking)
- `mediapipe` (For hand tracking via MediaPipe)

To install all dependencies at once, use the following command:
```bash
pip install pyfirmata opencv-python cvzone mediapipe
```

---

## Hardware Requirements

1. Arduino board (e.g., Arduino Uno)
2. USB cable to connect the Arduino to the computer
3. Additional components (depending on your Arduino setup)

Ensure the **StandardFirmata** sketch is uploaded to your Arduino:
1. Open the Arduino IDE.
2. Go to `File > Examples > Firmata > StandardFirmata`.
3. Select the correct board and COM port.
4. Upload the sketch to your Arduino.

---

## Setting Up the Project

1. Clone the repository:
```bash
git clone https://github.com/yourusername/arduino-hand-tracking-controller.git
```

2. Navigate to the project directory:
```bash
cd arduino-hand-tracking-controller
```

3. Ensure Python 3.10.0 is installed and added to your PATH.

4. Install the required Python libraries (as mentioned above).

---

## Running the Project

1. Connect your Arduino board to the computer.
2. Identify the COM port assigned to your Arduino (e.g., `COM3`).
3. Open the `controller.py` file and update the `comport` variable with the correct COM port:
   ```python
   comport = "COM3"  # Replace with the actual COM port
   ```
4. Run the script:
   ```bash
   python controller.py
   ```

---

## Notes

- This project is compatible **only with Python 3.10.0**.
- Ensure all required dependencies are installed before running the script.
- If you encounter issues with COM port access, ensure no other program (e.g., Arduino IDE Serial Monitor) is using the port.

---

## Resources

1. [PyFirmata Documentation](https://github.com/tino/pyFirmata)
2. [OpenCV Documentation](https://docs.opencv.org/)
3. [CvZone GitHub Repository](https://github.com/cvzone/cvzone)
4. [MediaPipe Documentation](https://google.github.io/mediapipe/solutions/hands)

---

## License

This project is open-source and available under the [MIT License](LICENSE).


Circuit Description:
Arduino Ground Pin (GND): Connect to the ground (GND) rail of the breadboard.
LEDs:
The cathode (short leg) of each LED is connected to the ground rail of the breadboard.
The anode (long leg) of each LED is connected to individual resistors.
Resistors: Use a 220Ω resistor for each LED. One end of each resistor is connected to the anode of an LED, and the other end is connected to an Arduino digital pin.
Arduino Digital Pins:
D8 → LED 1
D9 → LED 2
D10 → LED 3
D11 → LED 4
D12 → LED 5



Text-Based Circuit Diagram:
sql
Copy
Edit
Arduino       Breadboard
-------       -----------
 GND ---------> Ground Rail
 D8  ---------> Resistor → Anode of LED 1
 D9  ---------> Resistor → Anode of LED 2
 D10 ---------> Resistor → Anode of LED 3
 D11 ---------> Resistor → Anode of LED 4
 D12 ---------> Resistor → Anode of LED 5
 Cathodes of all LEDs --> Ground Rail
