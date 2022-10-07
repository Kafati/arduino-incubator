![INCUBATOR](https://user-images.githubusercontent.com/81776578/113349963-7af58480-9341-11eb-91d2-7131291e2002.png)
# arduino-incubator
simple design for an icubator using common breakout boards
six parameters are set through the matrix keypad:
- "Temp Off","degC",
- "Temp On","degC",
- "Turn active","Y/N",
 - "Humidity","%",
 - "Frequency","hrs",
 - "turn stop","day".

## Temperature control 
The temperature control system uses a feedback on off controller based on a SPDT relay and DS18B20 temperature sensor to maintain the set temperature .
## Turning mechanism
A crack mechanism driven by a synchronous ac motor is used to turn the trays. Given the motor rpm as 5 revolutions per minute, the angular position of the crank can be translated to a particular inclination . Switching the motor on for some seconds say 6 second will get the crank to the top dead centre and another 6 seconds will get it to  the bottonm dead centre. The interval between these successive turns can be set through the lcdc menu. After 18  days ,the turning mechanism should be stopped, this can be achieved using lcd menu

 
  A tone buzzer is included to sound an alarm should there be a deviation from the set parameters.
## Libraries used
the following libraries were used in development.
- paulstoffregen/OneWire@^2.3.5
- milesburton/DallasTemperature@^3.9.1
- chris--a/Keypad@^3.1.1
- adafruit/RTClib@^1.12.5
- adafruit/DHT sensor library@^1.4.2
- paulstoffregen/TimerOne@^1.1
- sstaub/Ticker@^4.2.0
- marcoschwartz/LiquidCrystal_I2C@^1.1.4
- adafruit/Adafruit Unified Sensor@^1.1.4


