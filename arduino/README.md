# Arduino ↔ RC522 Connection

| RC522 Pin | Arduino Uno Pin |
| --------- | --------------- |
| SDA (SS)  | 10              |
| SCK       | 13              |
| MOSI      | 11              |
| MISO      | 12              |
| RST       | 9               |
| GND       | GND             |
| VCC       | 5V              |

# Run Command
```besh
cd ~/Downloads
chmod +x arduino-ide_*.AppImage
./arduino-ide_*.AppImage
```
```besh
arduino-ide
```
```besh
ls /dev/ttyACM*
```

# Fix Permission
```besh
sudo usermod -aG dialout $USER
```
