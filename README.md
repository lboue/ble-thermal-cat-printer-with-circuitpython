# BLE Thermal "Cat" Printer with CircuitPython

### Overview
[BLE Thermal "Cat" Printer with CircuitPython](https://learn.adafruit.com/ble-thermal-cat-printer-with-circuitpython)

## BLE

### Introduction to Bluetooth Low Energy
 * [Introduction to Bluetooth Low Energy](https://learn.adafruit.com/introduction-to-bluetooth-low-energy)

### BLE Sniffer with nRF52840
 * [BLE Sniffer with nRF52840](https://learn.adafruit.com/ble-sniffer-with-nrf52840)


### Adafruit BLE Library
 * [Adafruit BLE Library](https://docs.circuitpython.org/projects/ble/en/latest/api.html)

**Scanning MX10**
 * [ble_detailed_scan.py](https://github.com/adafruit/Adafruit_CircuitPython_BLE/blob/main/examples/ble_detailed_scan.py)
```
scanning
<Address 1a:11:27:26:bd:03> <ProvideServicesAdvertisement flags=<AdvertisingFlags general_discovery le_only > services=<BoundServiceList: UUID(0xaf30)> >
	Advertisement(data=b"\x03\x03\x30\xaf\x02\x01\x06")
```

### Using The MX10 Thermal Printer

* Power on the printer (you can tell it's powered on when the blue LED blinks), then power on your CLUE.
* The CLUE will wait until it can connect to the printer.
* Tap the "UP" button to move to the next file in the list. When you reach the end of the list, you'll be sent back to the first file.
* Tap the "DOWN" button to send the selected file to the printer. While the print is in progress, button presses are ignored.
* When the image is done printing, the CLUE will return to the screen where you can select an image to print.
