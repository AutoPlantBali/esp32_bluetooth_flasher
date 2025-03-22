# Arduino Bluetooth Flasher
Arduino programming with Bluetooth using ESP32 makes it easy to upload code to Arduino without any problems with the serial port.
# Wiring

| ESP32 PIN   | LOGIC LEVEL CONVERTER | ARDUINO PIN |
|:-----------:|:---------------------:|:-----------:|
| RX          | LV1 <------> HV1      | TX          |
| TX          | LV2 <------> HV2      | RX          |
| 3V3         | LV  <------> HV       | 5V          |
| GND         | GND <------> GND      | GND         |
| D26         | LV3 <------> HV3      | RST         |

![logic_level_converter](/doc/logic_level_converter.png)        

![wiring](/doc/wiring.png)

# Setup ESP32
* Flash From PC
  1. Download [Flash Download Tool](https://dl.espressif.com/public/flash_download_tool.zip)
  2. Connect ESP32 Board to PC
  3. ChipType select ESP32 and klik OK
  ![flash_download_tool_1](/doc/flash_download_tool_1.png)
  4. Browse file firmware_0x10000.bin and input address offset 0x10000. Next, select the COM port and click START.
  ![flash_download_tool_2](/doc/flash_download_tool_2.png)

* Flash From Android
  1. Install [ESP32 Loader (Blynk Uploader)](https://play.google.com/store/apps/details?id=com.bluino.esp32loader&pcampaignid=web_share)
  2. Connect ESP32 Board to phone using OTG cable
  3. Browse file firmware_0x10000.bin and klik icon upload
  ![esp32_loader](/doc/esp32_loader.png)

# Programming Arduino
  Default programmer baudrate 115200, if you need change to 57600 connect PIN 13 to GND.
  Support [Bluino Loader - Arduino IDE](https://play.google.com/store/apps/details?id=com.bluino.bluinoloader&pcampaignid=web_share) for Android phone.

  | Board                                               | Baudrate Programming  | Need Logic Level |
  |:----------------------------------------------------|:---------------------:|:----------------:|
  | Arduino/Genuino Uno                                 | 115200                | YES              |
  | Arduino/Genuino Mega w/ ATmega2560                  | 115200                | YES              |
  | Arduino Nano w/ ATmega328P                          | 115200                | YES              |
  | Arduino Nano w/ ATmega328P (old)                    | 57600                 | YES              |
  | Arduino Pro or Pro Mini (5V, 16 MHz) w/ ATmega328P  | 57600                 | YES              |
  | Arduino Pro or Pro Mini (3.3V, 8 MHz) w/ ATmega328P | 57600                 | NO               |
  | Arduino Duemilanove or Diecimila w/ ATmega328P      | 57600                 | YES              |

  [![Arduino Programming Over Bluetooth (ESP32)](https://img.youtube.com/vi/-EZQ4JxbSUI/0.jpg)](https://www.youtube.com/watch?v=-EZQ4JxbSUI "Arduino Programming Over Bluetooth (ESP32)")

# Debug
  Open ESP32 serial2 port set baudrate 115200.
