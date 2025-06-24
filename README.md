# Temperature-Monitoring-System

INTRO : 

This project involves developing a Temperature Monitoring System using an Arduino Uno, a TMP36 analog temperature sensor, and a 16x2 LCD display with an I2C interface. The system is designed to measure ambient temperature in real time and display the output on an LCD screen. It demonstrates key embedded system concepts such as analog-to-digital conversion, sensor interfacing, and communication using the I2C protocol.


Temperature Sensor : 

The TMP36 is a widely used, low-voltage, analog temperature sensor from Analog Devices. It is part of the TMP3x series, known for its accuracy, stability, and ease of use. The sensor does not require any external calibration or additional circuitry. It operates within a voltage range of 2.7V to 5.5V, making it ideal for microcontroller-based applications like this one. The sensor provides a linear output of 10 mV per °C, with 500 mV corresponding to 0°C and 750 mV for 25°C. Its operating temperature range is from –40°C to +125°C, and it has a typical accuracy of ±2°C.
The sensor’s output pin is connected to the Arduino’s analog pin A0. The Arduino Uno features a 10-bit Analog-to-Digital Converter (ADC), which converts the analog voltage from the sensor into a digital value between 0 and 1023. This value is then used to calculate the actual voltage using:

Voltage = (analogValue × 5.0) / 1023.0

From this voltage, the temperature in Celsius is calculated using the formula:

Temperature (°C) = (Voltage – 0.5) × 100

The system takes a new reading every second to keep the temperature display updated in real time.


To display the measured temperature, a 16x2 LCD is used with an I2C backpack. The I2C (Inter-Integrated Circuit) protocol is a widely used communication standard that enables multiple devices to communicate over just two wires: Serial Data Line (SDA) and Serial Clock Line (SCL). In this project, I2C simplifies the connection between the Arduino and the LCD by reducing the number of pins required, which helps minimize wiring complexity and makes the design cleaner and more efficient. The Arduino acts as the master device, controlling the clock and data lines, while the LCD with the I2C interface acts as the slave device. This protocol also allows multiple devices to share the same bus, enabling easy expansion with other sensors or modules in the future.

The LCD clearly displays the current temperature in degrees Celsius, and the same data is also sent to the Serial Monitor for verification or future expansion.


Components Used :
1. Arduino Uno – Main microcontroller board
2. TMP36 Temperature Sensor – Analog sensor with 10 mV/°C sensitivity
3. 16x2 I2C LCD – For real-time temperature display
4. Breadboard and Jumper Wires – For building the circuit
5. USB Cable – For code upload and power supply

This system is accurate, efficient, and beginner-friendly. It can be extended further to include data logging, alert systems, or wireless monitoring using Bluetooth or Wi-Fi. Its modular nature allows easy integration into broader applications such as smart thermostats, weather stations, or industrial monitoring setups.

The project provided hands-on experience in sensor calibration, analog signal handling, and communication protocols in embedded systems. As part of the internship, it was a valuable learning opportunity, combining both hardware and software skills in a practical, real-time application.
