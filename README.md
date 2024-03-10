# BLE Thermal "Cat" Printer with CircuitPython

* [Bluetooth 'cat' thermal printer review By Jo Hinchliffe](https://hackspace.raspberrypi.com/articles/bluetooth-cat-thermal-printer-review)

The printer has an internal battery, which needs charging via a micro USB cable (included). Once charged
 * Single button press (there is only one button) turns the unit on.
 * Double-pressing the button causes the printer to print a test page that features a QR code and some details, including the device Bluetooth name and the pairing PIN.

### Overview
[BLE Thermal "Cat" Printer with CircuitPython](https://learn.adafruit.com/ble-thermal-cat-printer-with-circuitpython)

## BLE

### Introduction to Bluetooth Low Energy
 * [Introduction to Bluetooth Low Energy](https://learn.adafruit.com/introduction-to-bluetooth-low-energy)

### BLE Sniffer with nRF52840
 * [BLE Sniffer with nRF52840](https://learn.adafruit.com/ble-sniffer-with-nrf52840)
 * [nRF Sniffer for Bluetooth LE](https://infocenter.nordicsemi.com/index.jsp?topic=%2Fug_sniffer_ble%2FUG%2Fsniffer_ble%2Finspecting_data.html)
 	* [Download nRF Sniffer for Bluetooth LE](https://www.nordicsemi.com/Products/Development-tools/nrf-sniffer-for-bluetooth-le/download#infotabs)
 	* [nRF Connect SDK IEEE 802.15.4 Sniffer](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/samples/peripheral/802154_sniffer/README.html#building_and_running)

### Adafruit BLE Library
 * [Adafruit BLE Library](https://docs.circuitpython.org/projects/ble/en/latest/api.html)

**Scanning MX10**
 * [ble_detailed_scan.py](https://github.com/adafruit/Adafruit_CircuitPython_BLE/blob/main/examples/ble_detailed_scan.py)
```
scanning
<Address 1a:11:27:26:bd:03> <ProvideServicesAdvertisement flags=<AdvertisingFlags general_discovery le_only > services=<BoundServiceList: UUID(0xaf30)> >
	Advertisement(data=b"\x03\x03\x30\xaf\x02\x01\x06")
```

## Using The MX10 Thermal Printer

* Power on the printer (you can tell it's powered on when the blue LED blinks), then power on your CLUE.
* The CLUE will wait until it can connect to the printer.
* Tap the "UP" button to move to the next file in the list. When you reach the end of the list, you'll be sent back to the first file.
* Tap the "DOWN" button to send the selected file to the printer. While the print is in progress, button presses are ignored.
* When the image is done printing, the CLUE will return to the screen where you can select an image to print.

### Thermal Printer Demo
 
 * Thermal Printer Demo](https://github.com/bitbank2/Thermal_Printer/blob/master/examples/Thermal_Printer_Demo/Thermal_Printer_Demo.ino)

Logs
```
17:13:19.058 -> Scan Result: Name: MX10, Address: 1a:11:27:26:bd:03, manufacturer data: 1a112726bd03, serviceUUID: 0000af30-0000-1000-8000-00805f9b34fb, rssi: -52 
17:13:19.090 -> Found a match for MX10
17:13:19.090 -> Printer type = 2
17:13:19.090 -> A match! - 1a:11:27:26:bd:03 - MX10
17:13:23.618 -> Found a compatible device - MX10
17:13:23.618 -> Found a printer!, connecting...
17:13:23.618 ->  - Created client, connecting to 1a:11:27:26:bd:03
17:13:24.208 -> Came back from connect
17:13:24.706 ->  - Found our service
17:13:24.706 -> Got data transfer characteristic!
17:13:24.706 -> Connected!, printing graphics
17:13:27.650 -> Testing plain text printing
17:13:27.875 -> Disconnecting
17:13:27.875 -> Done!
```
