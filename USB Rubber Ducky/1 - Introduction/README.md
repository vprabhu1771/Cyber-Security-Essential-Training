# USB Rubber Ducky - Programming Guide

## Introduction
The USB Rubber Ducky is a powerful keystroke injection tool used for penetration testing and automation. This guide provides step-by-step instructions on how to program and deploy a script using the USB Rubber Ducky.

## Requirements
- USB Rubber Ducky
- A computer with a USB port
- Ducky Script knowledge (basic keystroke commands)
- Encoder software (Duck Toolkit or Hak5 Encoder)

## Steps to Program the USB Rubber Ducky

### 1. Connect the USB Rubber Ducky
Insert your USB Rubber Ducky into an available USB port on your computer.

### 2. Download and Install the Encoder Software
Choose and install one of the following tools for encoding Ducky Script:
- [Duck Toolkit](https://github.com/kevthehermit/DuckToolkit)
- [Hak5 Encoder](https://github.com/hak5darren/USB-Rubber-Ducky)

### 3. Write Your Ducky Script
Create a script using Ducky Script, which consists of keystroke commands to execute desired actions. Example:
```
DELAY 1000
GUI r
DELAY 500
STRING notepad
ENTER
DELAY 500
STRING Hello, USB Rubber Ducky!
ENTER
```
Save the script as `payload.txt`.

### 4. Encode the Script
- Open the encoder software.
- Load `payload.txt` into the tool.
- Select the appropriate encoding options for your target operating system.
- Click "Encode" to generate the `inject.bin` payload.

### 5. Copy the Payload to the USB Rubber Ducky
- Remove the microSD card from the USB Rubber Ducky.
- Insert it into a card reader.
- Copy the `inject.bin` file to the root directory of the microSD card.
- Eject the card safely and reinsert it into the USB Rubber Ducky.

### 6. Deploy the USB Rubber Ducky
- Insert the USB Rubber Ducky into the target computer.
- The payload will execute automatically.

## Disclaimer
This tool should only be used for ethical security testing and authorized automation purposes. Unauthorized use may violate laws and policies.

## References
- [Hak5 Official Documentation](https://docs.hak5.org/)
- [Ducky Script Reference](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Duckyscript)

