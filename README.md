# NTC_temperature_sensor_reading_function
# NTC Thermistor Temperature Sensor with Serial Threshold

A precision temperature measurement system using a 10k NTC Thermistor. The system calculates temperature using the B-parameter Steinhart-Hart equation and features interactive threshold setting.

## 🚀 Features
* **Oversampling:** Takes 100 samples per reading to filter out electrical noise.
* **Power Efficient:** Uses a digital pin (`D2`) to power the sensor only when reading.
* **Interactive:** Set a `TempThreshold` dynamically via the Serial Monitor.
* **High Precision:** Outputs data with 3 decimal places.

## 🛠 Hardware Required
* Arduino Board (e.g., Uno, Nano) or ESP32
* 10k NTC Thermistor
* 10k Ohm Resistor (Voltage Divider R1)
* Jumper wires and breadboard

## 📉 Circuit Diagram Logic
The sensor is wired in a voltage divider configuration:
* **Pin 2 (Output):** Supplies power to the divider.
* **Pin 34 (Input):** Reads the voltage between the 10k resistor and the NTC.
* **Ground:** Completes the circuit.



## 💻 Configuration
Before uploading, verify these constants in the code to match your specific hardware:
* `voltageDividerR1`: The actual measured resistance of your static resistor.
* `BValue`: Check your NTC datasheet (commonly 3435 or 3950; this code uses 3576).
* `samplingrate`: Increase for stability, decrease for speed.

## 🚦 How to Use
1. Open the **Serial Monitor** at **115200 baud**.
2. The current temperature will print automatically.
3. Type a number in the input bar and press **Enter** to update the internal `TempThreshold`.

