## Raspberry Pi 4B ↔ RC522 Connection

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
