# LiveStreamControlCar

This project utilises the ESP32 CAM module to create a remote-controlled car with real-time video streaming capabilities, controllable over Wi-Fi via a web interface. This setup is ideal for applications in surveillance, exploration, and automation.

## Features

- **Real-Time Video Feed**: Streams live video from the ESP32 CAM module to the web interface.
- **Remote Control**: Car movement and camera views are controllable over a local network using a web interface.
- **Web Interface**: User-friendly web-based control panel with live video, directional controls, and status updates.
- **Low-Latency Operation**: Efficient video and data transmission for smooth real-time control.

## Components

- **ESP32 CAM Module**: Provides the processing power and camera feed.
- **Motor Driver (L298N)**: Controls the car’s motors.
- **DC Motors**: Enable car movement in all directions.
- **Power Supply**: Battery to power the ESP32 CAM and motors.
- **Chassis and Wheels**: Structure of the car for navigation.
  
## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ShivamBaharwani/LiveStreamControlCar.git
   cd LiveStream Control Car
   ```

2. **Configure the ESP32 CAM**:
   - Install [Arduino IDE](https://www.arduino.cc/en/software) and set up the ESP32 board package.
   - Connect the ESP32 CAM module to your computer.
   - Open `Car.ino` in Arduino IDE.

3. **Network Configuration**:
   - In the Arduino code, update the Wi-Fi credentials to match your local network:
     ```cpp
     const char* ssid = "Your_SSID";
     const char* password = "Your_PASSWORD";
     ```

4. **Upload the Code**:
   - Select the ESP32 board in Arduino IDE, then upload the code to the ESP32 CAM.

5. **Build the Circuit**:
   - Connect the ESP32 CAM to the motor driver and DC motors as specified in the circuit diagram.
   - Ensure proper power supply connections for stable operation.

6. **Access the Web Interface**:
   - After uploading, find the ESP32 CAM’s IP address by checking your router's connected devices.
   - Open the IP address in a web browser to access the control panel.

## Usage

1. **Power On**: Turn on the power supply to the ESP32 CAM and motor driver.
2. **Connect**: Use any device with Wi-Fi to connect to the same network and access the web interface.
3. **Control**: Use the on-screen controls for car movement, and view the real-time video stream for navigation.

## Project Structure

- **Car.ino**: The main Arduino code for controlling the car and streaming video.
- **/Diagrams**: Documentation and circuit diagrams.

## Circuit Diagram

Refer to the `Diagrams` folder for detailed circuit diagrams and connection layouts.

## Requirements

- Arduino IDE (for code upload)
- ESP32 board package
- Hardware components: ESP32 CAM, L298N motor driver, DC motors, battery, chassis, etc.

## Troubleshooting

- **No Video Stream**: Check the camera connection, ensure the ESP32 CAM is connected to Wi-Fi, and verify the IP address.
- **Delayed Controls**: Ensure a strong Wi-Fi signal for optimal performance.
- **Upload Errors**: Confirm correct board selection and USB connection in the Arduino IDE.

## Future Enhancements

- **Obstacle Detection**: Integrate ultrasonic sensors for automatic obstacle avoidance.
- **Mobile App**: Create a dedicated mobile app for easier control.
- **Long-Range Control**: Implement external servers for remote control beyond local network limitations.
