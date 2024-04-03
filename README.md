# esphome-fence-gate-sensor
This project uses an ESP board to create a fence gate sensor utilizing the ESPHome add-on and integration in Homeassistant. The configuration will report status on gate open or closed, has a restart button in Homeassistant, as well as wifi connectivity status via the blue LED. The three LED's on the board (and their corresponding code in the config file) are completely optional but are useful for troubleshooting the physical installation.
<p><img src="https://github.com/cyclone182/esphome-fence-gate-sensor/blob/main/ESPHome-fence-gate-sensor.jpg" width="200" /></p>
<p></p><img src="https://github.com/cyclone182/esphome-fence-gate-sensor/blob/main/ESPHome-fence-gate-sensor-inside.jpg" width="200" /></p>

<p>The following was done on an ESP8266 board, however it should work with a ESP32 with some tweaking.</p>
<p>For this project you will need the ESP board, small prototype board, jumper wire, usb power supply, waterproof magnetic reed switch, three different colored LED's, and three appropriate resistors for the LED's you selected.</p>
<p>Instructions:</p>
<p>1. Wire the reed switch from GPIO04 to GND.</p>
<p>2. Wire the red LED and resistor from GPIO16 to GND.</p>
<p>3. Wire the green LED and resistor from GPIO05 to GND.</p>
<p>4. Wire the blue LED and resistor from GPIO014 to GND.</p>
<p>5. Prepare the config.yaml file from this repository by editing your api key, ota password, and the fallback hotspot AP password.</p>
<p>6. Upload the config file to your ESP board.</p>
<p>7. Once the config is loaded, it should take 10s for the blue LED report Wifi status.</p>
<p>8. The red and green LED's should now report switch state changes. These changes should also be visible in Homeassistant.</p>
