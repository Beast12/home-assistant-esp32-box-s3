# ESP32-S3 Box Office 📦🎤

Welcome to the ESP32-S3 Box Office project! This repository contains the configuration and code for setting up an ESP32-S3 Box as a voice assistant. The device will respond to the wake word "hey_jarvis" and provide various voice-controlled functionalities.

The yaml file is a combination of 2 files:

<https://github.com/esphome/firmware>:

* <https://github.com/esphome/firmware/blob/main/wake-word-voice-assistant/esp32-s3-box-3.yaml>
* <https://github.com/esphome/issues/issues/5296>

The first is so that the "Wake word engine location" is available in Home Assistant
The second one is so that the sensors are available

The pictures used are chatgpt's interpretation of Jarvis...

## Features ✨

- **Voice Activation**: Uses "hey_jarvis" as the wake word.
- **Illustrations**: Different states like idle, listening, thinking, replying, and error are visually represented.
- **Customizable Background Colors**: Changeable background colors for various states.
- **Static IP Configuration**: Manual network settings to ensure stable connectivity.
- **API and OTA Support**: Secure API connections and Over-the-Air updates.
- **Touchscreen and Buttons**: Interactive interface using GT911 touchscreen and GPIO buttons.
- **Radar Motion Detection**: Detects motion using the AT581x radar sensor.

## Setup Instructions 🚀

### Prerequisites

- **ESP32-S3 Box**

- **ESPHome** installed on your local machine or accessible via Home Assistant

### Configuration

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/esp32-s3-box-office.git
   cd esp32-s3-box-office
   ```

2. **Modify Secrets**
   Ensure you have a `secrets.yaml` file in your ESPHome directory with the following entries:
   ```yaml
   wifi_ssid: "your_wifi_ssid"
   wifi_password: "your_wifi_password"
   web_password: "your_web_password"
   api_token: "your_api_token"
   ```

3. **Deploy Configuration**
   Deploy the configuration to your ESP32-S3 Box via ESPHome Dashboard or using the command line:
   ```bash
   esphome run esp32-s3-box-office.yaml
   ```

### Illustrations and Colors

The project uses specific illustration files for different states. Ensure these files are located in the `voice_assistant_gfx` directory:
- `loading.png`
- `idle.png`
- `listening.png`
- `thinking.png`
- `replying.png`
- `error.png`

### Network Configuration

Set the static IP and network details according to your network setup:
```yaml
ip: "192.168.1.51"
gw: "192.168.1.1"
subnet: "255.255.255.0"
dns: "192.168.1.1"
```

## Components Used 🧩

- **AHTxx**: Temperature and Humidity sensor.
- **ESP-ADF**: Audio Development Framework for handling microphone and speaker.
- **AT581x**: Radar sensor for motion detection.
- **GT911**: Touchscreen controller.
- **ILI9xxx**: Display driver for the LCD.

## Security 🔒

- **WiFi Credentials**: Ensure WiFi credentials are securely stored in the `secrets.yaml`.
- **API Encryption**: Secure communication with the device using the API token.
- **Web Authentication**: Protect the web server with a username and password.

## Troubleshooting 🛠️

- **No WiFi Connection**: Ensure SSID and password are correct in the `secrets.yaml`.
- **API Connection Issues**: Verify the API token and network configuration.
- **Illustration Errors**: Check that all illustration files are correctly named and placed in the `voice_assistant_gfx` directory.

## Contribution 🤝

We welcome contributions! Feel free to submit issues, fork the repository, and create pull requests. Let's make this project even better together!


**Happy Coding!** 🎉

---
