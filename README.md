# LVGL ESPhome Guition ESP32-S3-4848S040 custom firmware

> [!NOTE]
>
> ❤️ **GOOD NEWS**
>
> You can use any ESPHome version, including 2025.6+. See the [instructions](#-installation) below for details.

<p align="center">
 <img width="200px" src="/doc/img/screen1.png">
 <img width="200px" src="/doc/img/screen2.png">
 <img width="200px" src="/doc/img/screen3.png">
 <img width="200px" src="/doc/img/screen4.png">
 <img width="200px" src="/doc/img/screen5.png">
 <img width="200px" src="/doc/img/screen6.png">
 <img width="200px" src="/doc/img/screen7.png">
 <img width="200px" src="/doc/img/screen8.png">
 <img width="200px" src="/doc/img/screen9.png">
 <img width="200px" src="/doc/img/screen10.png">
 <img width="200px" src="/doc/img/screen12.png">
</p>

<p align="center">
    <img alt="Static Badge" src="https://img.shields.io/badge/made%20by-alaltitov-blue">
    <img alt="Static Badge" src="https://img.shields.io/badge/version-v1.0%20Beta-green">
    <img alt="Static Badge" src="https://img.shields.io/badge/esphome min version-2025.5.2-red">
    <img alt="Static Badge" src="https://img.shields.io/badge/license-MIT-orange">
</p>

## ✨ Features

- Status indicators for Wi-Fi, Home Assistant, thermostat, air conditioner, touchscreen lock
- Weather icons with current conditions and temperature
- Date and time
- Sensor readings from Home Assistant
- Thermostat control with built-in display relay
- Air Conditioner control with built-in display relay
- Vacuum control
- Shutter control
- Media player control
- Control of lights
- Settings:
  * Backlight adjustment
  * Screen timeout settings
  * Language selection for states

## 📦 Installation
> [!WARNING]
> All widgets are fully supported only on ESPHome firmware version **2025.5.2**.  
>  
> It is possible to run this project on the latest ESPHome version, but you will need to comment out one of the widgets and button in devices.yaml (it has been tested to work without the shutter or media player widgets).  
>  
> Unfortunately, ESPHome versions **2025.6 and newer** cannot handle this number of widgets on this device.


<img width="600px" src="/doc/img/screen13.png">
<img width="200px" src="/doc/img/screen14.png">

```bash
pip install esphome==2025.5.2
esphome run main.yaml --device COM9
esphome run main.yaml --device OTA
```


> 📹 **Video [instruction](https://youtu.be/HYN_2hvcbes?si=JfYQH4vCuFlr8Q9r)**

<img width="400px" src="/doc/img/screen11.png">

- You must enable the "Allow the device to perform Home Assistant actions." option in the ESPHome integration to Home Assistant to control devices.
- Install custom component for translations and covers for media player from [here](https://github.com/alaltitov/homeassistant-display-tools).
- Copy repository to vscode or to esphome folder of your Home Assistant. Change in substitutions your entities in all widgets (only in substitution, in code everything will be substituted automatically).

## 🐛 Known Issues
- The weather status text does not change depending on day/night, only the picture
- When the connection with the API is lost/reboot, the screen lock state is not restored
- When initially loading/flashing, it may go into reboot (I have not yet found the cause of the problem)

## ⚠️ Important Notice
- Regarding shutter and vacuum widgets: Testing was conducted on demo entities (as I don't have real devices), so errors may occur when working with real entities. Feedback is welcome! 🙏

## 📖 Documentation

- https://esphome.io/components/lvgl/

## 🤝 Thanks for your help

- Thanks, [сlydebarrow](https://github.com/clydebarrow), [jesserockz](https://github.com/jesserockz), [ssieb](https://github.com/ssieb) for helping me with the project!

## 💝 Support the Project
This project was made in my free time and if it was useful to you, you can support me if you find it necessary 😊:

**ETH/USDT (ERC-20):** `0x9fF0E16a58229bEcdFDf47d9759f20bE77356994`

Or just put ⭐ Thank you
