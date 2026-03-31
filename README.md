# SimGpsTransmitter

An Arduino sketch that reads GPS coordinates from a NEO-6M GPS module and transmits them to a web server at configurable intervals via HTTP GET requests through a SIM800L GSM/GPRS module. Useful as a lightweight IoT vehicle tracker.

## Features

- Reads NMEA data from a NEO-6M GPS module over SoftwareSerial
- Parses latitude and longitude using the TinyGPS++ library
- Transmits location data to a configurable web server via HTTP GET over GPRS (SIM800L)
- Configurable transmission frequency (default: 15 seconds)
- Error LED indicator for GSM connection issues
- Configurable APN, server IP, and logging password

## Tech Stack

- C++ (Arduino)
- SIM800L GSM/GPRS module
- NEO-6M GPS module
- [TinyGPS++ library](http://arduiniana.org/libraries/tinygpsplus/)
- SoftwareSerial

## Project Structure

| File | Description |
|---|---|
| `SimGpsTransmitter.ino` | Main Arduino sketch |

## Hardware Connections

| Pin | Connection |
|---|---|
| Pin 3 | GPS module RX |
| Pin 4 | GPS module TX |
| Pin 5 | SIM module TX |
| Pin 6 | SIM module RX |
| Pin 10 | Error LED |
| Pin 12 | SIM connection indicator |

## Requirements

- Arduino IDE
- [TinyGPS++ library](http://arduiniana.org/libraries/tinygpsplus/) (install via Library Manager)
- NEO-6M GPS module
- SIM800L module with active SIM card and data plan

## Setup

1. Install TinyGPS++ via the Arduino Library Manager.
2. Configure `apn`, `loggingPassword`, and `serverIP` in the sketch.
3. Upload to an Arduino board and open the Serial Monitor at 9600 baud.

## License

MIT
