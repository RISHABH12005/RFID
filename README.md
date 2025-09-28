# RFID (RC522)
This project demonstrates how to interface an *RC522 RFID reader* with a RPi using Python. The RC522 communicates over *SPI*.

## Hardware Required
- RPi 4B
- RC522 RFID module
- Jumper wires
- RFID tags/cards

## GPIO (RFID → RPi GPIO)

| RFID GPIO | RPi GPIO |
|-----------|----------|
| SDA       | GPIO 8 (CE0)     |
| SCK       | GPIO 11 (SCLK)   |
| MOSI      | GPIO 10 (MOSI)   |
| MISO      | GPIO 9 (MISO)    |
| IRQ       | Not connected    |
| GND       | GND              |
| RST       | GPIO 25          |
| 3.3V      | 3.3V             |

## Features
- *Chip* : It is based on the MFRC522 integrated circuit from NXP Semiconductors.
- *Frequency* : Operates at 13.56 MHz.
- *Communication* : It can communicate with a microcontroller using the SPI protocol & also supports I2C & UART.
- *Reading* : The RC522 module emits a radio signal via its antenna.
- *Do not connect to 5V* The RC522 is a 3.3V device. 

## Setup on RPi
```bash
sudo raspi-config
# Go to: Interface Options → SPI → Enable
sudo reboot
```
```bash
ls /dev/spidev*
```
```bash
pip3 install spidev mfrc522
```

