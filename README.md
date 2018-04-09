# esp8266-button

Software which runs on a esp8266 and publishes a MQTT toppic which can
be used for different purpouses. I myself use it to toggle my flat in
a state where I'm sleeping in the evening and that I'm awake in the
morning an Home Assistant so it can automate different things accordingly.

## Getting the code

    git clone https://github.com/jeena/esp8266-button.git

## Hardware setup

![Hardware setup](https://github.com/jeena/esp8266-button/raw/master/espbutton-schema.png)

## Software setup

Open the espbutton/espbutton.ino file in the Arduino IDE.

It expects the credentials for your WiFi and MQTT in the file like this:

    #define ssid "myssid"
    #define password "mypass"
    #define mqtt_server "example.com"
    #define mqtt_port 1883
    #define mqtt_user "user"
    #define mqtt_password "passwd"
    #define topic "sensor/sleeping"
    #define topic_content "toggle"

Change the credentials so it matches your wifi and MQTT credentials. You
may also change the topic if it makes sense for you.

## Flashing

1. Under File -> Preferences set as Additional Boards Manager URLs:
   http://arduino.esp8266.com/versions/2.3.0/package_esp8266com_index.json
2. Chose under Tools -> Board the "Node MCU 1.0 (ESP12-E Module)"
3. Under Sketch -> Include Library -> Manage Libraries -> Search for
   "PubsubClient" and install the one "by Nick O'Leary" 
4. Press the Upload button

## Hardware Setup

t.b.d.

## License

This file is part of esp8266-temperature.

Copyright 2017 Jeena

esp8266-button is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

esp8266-button is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with esp8266-button. If not, see http://www.gnu.org/licenses/.
