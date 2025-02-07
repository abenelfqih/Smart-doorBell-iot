# Smart Doorbell IoT

## General Description

This smart doorbell project uses IoT technologies with an ESP32-CAM to detect when a person rings the doorbell, take a photo, and send it to a Telegram bot. Using `/lock` and `/unlock` commands, you can control the door's lock state through the Telegram bot.  Additionally, the project includes visualizations in ThingSpeak to display timestamps and the number of photos have been taken.


## Features

- Detects when someone rings the doorbell.
- Takes a photo of the person.
- Sends the photo to a Telegram bot.
- Controls the door lock via Telegram commands (`/lock` to lock, `/unlock` to unlock).
-  Visualizes timestamps and photo counts in ThingSpeak

## Hardware Requirements

- ESP32-CAM module
- Doorbell sensor (e.g., push button)
- solenoid lock
- TIP122 NPN Transistor
- diode 1N4007
- BreadBoard DC Jack
- Regulator 7805 5V
- Internet connection

## Software Prerequisites

- [Arduino IDE](https://www.arduino.cc/en/Main/Software)
- ESP32 board support package installed in Arduino IDE
- Libraries: `ESP32`, `WiFi`, `UniversalTelegramBot`
- ThingSpeak account and channel setup

## Installation Instructions

1. Clone this repository:
    ```bash
    git clone https://github.com/abenelfqih/smart-doorbell-iot.git
    cd smart-doorbell-iot
    ```
2. Open the `smart_doorbell.ino` file in Arduino IDE.

3. Install the necessary libraries:
    - Go to `Sketch` > `Include Library` > `Manage Libraries`.
    - Search for and install `UniversalTelegramBot`, `WiFi`, and any other required libraries.

4. Configure the WiFi and Telegram bot credentials in the `Esp32Cam_DoorBell.ino` file:
    ```cpp
    const char* ssid = "your-SSID";
    const char* password = "your-PASSWORD";
    const char* telegramToken = "your-telegram-bot-token";
    const char* chatID = "your-telegram-chat-id";
    ```

5. Connect the ESP32-CAM to your computer and upload the code.

## Usage

1. When someone rings the doorbell, a photo will be taken and sent to the Telegram bot.
2. To lock the door, send the `/lock` command to the Telegram bot.
3. To unlock the door, send the `/unlock` command to the Telegram bot.


