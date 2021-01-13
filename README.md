# HA SwitchPlate

The HA SwitchPlate is a user-programmable LCD touchscreen you can mount into a [standard North American work box](https://www.nema.org/Standards/ComplimentaryDocuments/NEMA%20WD%206%20-%20Dimensions%20for%20Wiring%20Devices%20-%20Excerpt.pdf) in place of a light switch.  It connects to your home automation system over WiFi to send and receive [MQTT](https://en.wikipedia.org/wiki/MQTT) messages in response to user interactions on the screen or events happening in your home.  The result is an attractive and highly-customizable controller for your home automation system which you can build yourself!

![HA SwitchPlate Models](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Three_Model_Variations.png?raw=true)

The HA SwitchPlate ("HASP") utilizes a [Nextion 2.4" LCD Touchscreen display](https://amzn.to/2TRTEU2) mounted in a 3D-printed enclosure as a touchscreen panel for home control and information display.  An [ESP8266-based microcontroller](https://amzn.to/2UZlga4) provides WiFi connectivity and system control.  The project has been developed to integrate with [Home Assistant](https://home-assistant.io/) and [OpenHAB](https://www.openhab.org/) but [should be compatible](Documentation/06_MQTT_Control.md) with any other MQTT-enabled automation platform such as [Domoticz](https://www.domoticz.com/wiki/MQTT), [Node-Red](http://noderedguide.com/tag/mqtt/), [Wink](https://github.com/danielolson13/wink-mqtt), [SmartThings](https://github.com/stjohnjohnson/smartthings-mqtt-bridge), [Vera](https://github.com/jonferreira/vera-mqtt), [HomeKit](https://www.npmjs.com/package/homekit2mqtt), etc.

The [Arduino code](Arduino_Sketch) for the ESP8266 provides a generic gateway between [MQTT](https://en.wikipedia.org/wiki/MQTT) and the [Nextion instruction set](https://www.itead.cc/wiki/Nextion_Instruction_Set).  A basic [Nextion HMI display file](Nextion_HMI) has been included with several pages of various layouts to provide user controls or to present information in response to MQTT messages sent to the device.

## Demo screens

![Scene controller](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_SceneController.png?raw=true) ![Status display](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_Status.png?raw=true) ![Media control](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_Media.png?raw=true) ![Alarm Panel](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_AlarmPanel.png?raw=true) ![Slider/Dimmer Controls](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_Dimmers.png?raw=true) ![HVAC Controls](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_HVAC.png?raw=true) ![Light toggles](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_LightToggles.png?raw=true) ![Fan controller](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/HASwitchPlate_Demo_FanControls.png?raw=true) ![WiFi Setup](https://github.com/aderusha/HASwitchPlate/blob/master/Documentation/Images/WiFi_Config_0.png?raw=true)

## Purchase an assembled unit

As this build requires some specialist skills and tools, I will occasionally be [offering assembled devices for sale here](https://www.tindie.com/products/luma/ha-switchplate-hasp-single-wide-assembled/).

## Buy me a coffee

[![Buy me a coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/gW5rPpsKR)

This project is powered by coffee.  [I might get a little weird about it at times](https://github.com/aderusha/RoastLearner), but it's not much of a stretch to suggest that coffee both powers and consumes a fair portion of my mental energy.  [Hook me up if you think HASP is cool](https://www.buymeacoffee.com/gW5rPpsKR).  Thanks!

## Bill of Materials

To build a simple version of this project you will minimally need the [Nextion display](https://amzn.to/2DIpahB) and the [WeMos D1 Mini](https://amzn.to/2Gc92Xs), 4 jumper wires, and a USB cable to power both devices.

A complete build that's ready to install will require the following components:

```
CHANGED Bom for European Version by PaulG4H 
```

* [Nextion 3.2" LCD Touchscreen display standard]
* [WeMos D1 Mini ESP8266 WiFi microcontroller](https://amzn.to/2UZlga4)
* [3D printed top](3d-print/Nextion_32_Top.stl)
* [3D printed base](3d-print/Nextion_32_Base.stl)
* Gira 55er double frame without middle like Gira #4010337002048 --> choose color and shape of frame you like
* Eight magnets round 5mm diameter, 2mm thick (http://www.amazon.de/dp/B07T13H3R5/)
* BME280 I2C temperature, humidity and air pressure sensor (http://www.amazon.de/dp/B07D8T4HP6/)
* BH1750 I2C lux sensor (http://www.amazon.de/dp/B07TPHCJNN/)
* [Mean Well IRM-03-5 AC to 5VDC Power supply](https://amzn.to/2UUWGa8)
* Level shifter for 3.3 to 5 volt serial connection to Nextion (http://www.amazon.de/dp/B07PY3CRFM/)


