A DIY, offline self-checkout trolley that uses RFID and Arduino to automate billing—ideal for rapid prototyping, smart retail concepts, and embedded innovation.

What It Does:
Scans RFID-tagged items in a shopping trolley
Calculates and displays item prices and total on LCD

Uses two buttons:
Confirm → Finalizes and resets bill
Remove → Deletes last scanned item

No cloud, no internet—fully offline system

3-second delay to avoid repeated scans

Powered by USB (power bank or battery)

Hardware:
Arduino Nano
MFRC-522 RFID Reader
16x2 LCD with I2C module
Piezo Buzzer
2 Push Buttons
Power Bank or 9V Battery

Pin Configuration
Component	Arduino Nano Pin
RFID       (SDA)	D10
RFID       (SCK)	D13
RFID       (MOSI)	D11
RFID       (MISO)	D12
RFID       (RST)	D9

LCD       (SDA)	A4
LCD       (SCL)	A5

Buzzer	   D3

Confirm Button	D4
Remove Button	D5

How It Works
RFID reader fetches 16-bit UID from card
UID is converted to integer → used as item price
LCD shows item price + running total
Buzzer beeps after each scan/action
Confirm resets total; Remove subtracts last item

Setup Guide:
Download or clone this repo
Open .ino file in Arduino IDE
Install required libraries: MFRC522, LiquidCrystal_I2C
Upload code to Arduino Nano
Power the system and test with RFID cards

Use Cases:

Smart shopping carts
DIY billing systems
RFID learning modules
Arduino project exhibitions
