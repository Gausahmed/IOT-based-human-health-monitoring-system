# IOT-based-human-health-monitoring-system
With tons of new healthcare technology start-ups, IoT is rapidly revolutionizing the healthcare industry. In this project, we have designed the IoT Based Patient Health Monitoring System using ESP8266 & Arduino. The IoT platform used in this project is ThingSpeak. ThingSpeak is an open-source Internet of Things (IoT) application and API to store and retrieve data from things using the HTTP protocol over the Internet or via a Local Area Network. This IoT device could read the pulse rate and measure the surrounding temperature. It continuously monitors the pulse rate and surrounding temperature and updates them to an IoT platform.

The Arduino Sketch running over the device implements the various functionalities of the project like reading sensor data, converting them into strings, passing them to the IoT platform, and displaying measured pulse rate and temperature on character LCD.
# Block diagram
![IoT-Based-Patient-Health-Monitoring-System-using-ESP8266-Arduino-1](https://user-images.githubusercontent.com/74852695/181570928-1432f5a1-2b18-434a-997c-ee96a3a31757.jpg)

This is a simple block diagram that explains the IoT Based Patient Health Monitoring System using ESP8266 & Arduino. Pulse Sensor and LM35 Temperature Sensors measure BPM & Environmental Temperature respectively. The Arduino processes the code and displays it to 16*2 LCD Display. ESP8266 Wi-Fi module connects to Wi-Fi and sends the data to IoT device server. The IoT server used here is Thingspeak. Finally, the data can be monitored from any part of the world by logging into the Thingspeak channel.

## Pulse Sensor
![pulse-sensor-lifeispreety com_-300x188](https://user-images.githubusercontent.com/74852695/181571311-d2fcb6f4-15cd-4a0b-ba86-de6a20832679.jpg)

The Pulse Sensor is a plug-and-play heart-rate sensor for Arduino. It can be used by students, artists, athletes, makers, and game & mobile developers who want to easily incorporate live heart-rate data into their projects. The essence is an integrated optical amplifying circuit and noise eliminating circuit sensor. Clip the Pulse Sensor to your earlobe or fingertip and plug it into your Arduino, you can ready to read heart rate. Also, it has an Arduino demo code that makes it easy to use.
The pulse sensor has three pins: VCC, GND & Analog Pin.
There is also a LED in the center of this sensor module which helps in detecting the heartbeat. Below the LED, there is a noise elimination circuitry that is supposed to keep away the noise from affecting the readings.

## LM35 Tempreature Sensor
The LM35 series are precision integrated-circuit temperature devices with an output voltage linearly-proportional to the Centigrade temperature. The LM35 device has an advantage over linear temperature sensors calibrated in Kelvin, as the user is not required to subtract a large constant voltage from the output to obtain convenient Centigrade scaling. The LM35 device does not require any external calibration or trimming to provide typical accuracies of ±¼°C at room temperature and ±¾°C over a full −55°C to 150°C temperature range.
![LM35-Temperature-Sensor-300x203](https://user-images.githubusercontent.com/74852695/181571729-f0fe8534-c0b0-43f8-b655-22ebd44dbcbf.jpg)

## ESP8266
The ESP8266 is a very user-friendly and low-cost device to provide internet connectivity to your projects. The module can work both as an Access point (can create hotspot) and as a station (can connect to Wi-Fi), hence it can easily fetch data and upload it to the internet making the Internet of Things as easy as possible. It can also fetch data from the internet using API’s hence your project could access any information that is available on the internet, thus making it smarter. Another exciting feature of this module is that it can be programmed using the Arduino IDE which makes it a lot more user-friendly.

![ESP8266-Pins-700x294](https://user-images.githubusercontent.com/74852695/181571902-186407bc-aec1-4bfd-a05c-b883f2b5c97b.png)

The ESP8266 module works with 3.3V only, anything more than 3.7V would kill the module hence be cautious with your circuits. Here is its pins description.

Pin 1: Ground: Connected to the ground of the circuit
Pin 2: Tx/GPIO – 1: Connected to Rx pin of programmer/uC to upload program
Pin 3: GPIO – 2: General purpose Input/output pin
Pin 4 : CH_EN: Chip Enable/Active high
Pin 5: Flash/GPIO – 0: General purpose Input/output pin
Pin 6 : Reset: Resets the module
Pin 7: RX/GPIO – 3: General purpose Input/output pin
Pin 8: Vcc: Connect to +3.3V only

## Circuit Diagram
For designing IoT Based Patient Health Monitoring System using ESP8266 & Arduino, assemble the circuit as shown in the figure below.
![Circuit-Diagram-768x466](https://user-images.githubusercontent.com/74852695/181572208-2ff43a5d-f649-4258-b42b-2ec38e0c556c.jpg)

1. Connect Pulse Sensor output pin to A0 of Arduino and other two pins to VCC & GND.
2. Connect LM35 Temperature Sensor output pin to A1 of Arduino and other two pins to VCC & GND.
3. Connect the LED to Digital Pin 7 of Arduino via a 220-ohm resistor.
4. Connect Pin 1,3,5,16 of LCD to GND.
5. Connect Pin 2,15 of LCD to VCC.
6. Connect Pin 4,6,11,12,13,14 of LCD to Digital Pin12,11,5,4,3,2 of Arduino.
7. The RX pin of ESP8266 works on 3.3V and it will not communicate with the Arduino when we will connect it directly to the Arduino. So, we will have to make a voltage divider for it which will convert the 5V into 3.3V. This can be done by connecting the 2.2K & 1K resistor. Thus the RX pin of the ESP8266 is connected to pin 10 of Arduino through the resistors.
8. Connect the TX pin of the ESP8266 to pin 9 of the Arduino.

## Setting thingspeak
ThingSpeak provides a very good tool for IoT based projects. By using the ThingSpeak site, we can monitor our data and control our system over the Internet, using the Channels and web pages provided by ThingSpeak. So first you need to sign up for ThingSpeak. So visit https://thingspeak.com and create an account.

![thinkspeak-sign-768x343](https://user-images.githubusercontent.com/74852695/181574110-040743b9-991d-40fd-9b2c-9a4a8c69b901.jpg)

Then create a new channel and set up what you want. The tutorial in the video below. Follow the video for more clarification.
Then create the API keys. This key is required for programming modifications and setting your data.
Then upload the code to the Arduino UNO by assembling the circuit shown above. Open the serial monitor and it will automatically connect to Wi-Fi and set up everything.
Now click on channels so that you can see the online data streaming, i.e IoT Based Patient Health Monitoring System using ESP8266 & Arduino as shown in the figure here.

## [Code](/Code.ino)

The source code for the project IoT Based Patient Health Monitoring System using ESP8266 & Arduino is given in the link above Click on Code heading. Write the code to your Arduino IDE, then compile it and upload it to your Arduino UNO Board.
