# RFI-Autologger

Version 1.2.1
<img width="1042" height="822" alt="image" src="https://github.com/user-attachments/assets/4ff9cc8d-4e9d-41ac-97b8-5151791a5861" />

## Overview

RFI Auto Logger is a Windows-based application designed to assist amateur radio operators, engineers, and RF investigators in mapping radio-frequency signal levels and interference sources while mobile or stationary.

The application combines radio signal readings with GPS position data and automatically generates KML and CSV files that can be imported into Google Earth, Google My Maps, CalTopo, GIS software, and spreadsheet applications.

The goal is to create a visual representation of signal strength across a geographic area to help identify interference sources, evaluate antenna performance, analyze coverage patterns, and document field measurements.

---

## Main Features

### Radio Support

Supported radio profiles:

* Yaesu FT-710
* Yaesu FT-891
* Yaesu FT-857
* Yaesu FT-817
* Thetis (Experimental)
* Yaesu FT-991A
* Yaesu FTDX10

The application communicates with radios using CAT control over a serial COM port.

---

### GPS Integration

* Automatic GPS detection and connection using the selected COM port
* NMEA GPS support
* GPS lock monitoring
* Real-time latitude and longitude display
* GPS status monitoring
* Automatic GPS reconnect capability

Supported GPS devices include:

* u-blox GPS receivers
* USB GPS receivers
* NMEA-compatible GPS devices

Default GPS baud rate:

```text
9600
```

---

### Signal Logging

The application records:

* Date and time
* Latitude
* Longitude
* Frequency
* Radio model
* Raw signal value
* Calculated S-meter value

Logging can be performed while:

* Driving
* Walking
* Stationary testing
* Mobile RFI hunting

---

### KML Export

Automatic generation of Google Earth and Google My Maps compatible KML files.

Signal levels are color-coded:

| Signal Level | Color  |
| ------------ | ------ |
| S0 – S2      | Green  |
| S3 – S5      | Yellow |
| S6 – S8      | Orange |
| S9           | Red    |
| S9+          | Purple |

This allows rapid visualization of signal hotspots and interference sources.

---

### CSV Export

CSV files are automatically generated and can be imported into:

* Microsoft Excel
* LibreOffice Calc
* Google Sheets
* GIS applications

Each logged point is immediately written to disk to reduce the risk of data loss.

---

### Voice Notifications

Optional voice notifications include:

* GPS locked
* GPS signal lost

Voice notifications can be enabled or disabled from the application settings.

---

### Automatic Settings Storage

The application automatically saves user preferences between launches, including:

* Radio selection
* Radio COM port
* Radio baud rate
* GPS COM port
* GPS baud rate
* Output folder
* Notification settings
* Window preferences

---

### About Screen

An integrated About screen provides application information and project credits.

---

## FT-710 Calibration

Version 1.2.1 includes improved FT-710 signal calibration based on field measurements collected using USB mode.

Current calibration reference points:

| RAW Value | S-Meter |
| --------- | ------- |
| 11        | S1      |
| 25        | S2      |
| 44        | S3      |
| 54        | S4      |
| 70        | S5      |
| 83        | S6      |
| 94        | S7      |
| 106       | S8      |
| 122       | S9      |
| 140       | S9+10   |
| 161       | S9+20   |
| 184       | S9+30   |
| 200       | S9+40   |

---

## Typical Applications

### Mobile RFI Hunting

Locate sources of:

* Electrical noise
* Power line interference
* Switching power supplies
* Solar inverter noise
* Broadband RF interference

### Coverage Mapping

Evaluate:

* Antenna performance
* Portable station coverage
* Mobile station coverage
* Signal propagation

### Field Engineering

Document RF measurements and create geographic signal maps for technical analysis.

---

## Future Enhancements

Planned or under consideration:

* Additional radio support
* SDR support (RTL-SDR)
* HackRF One support
* Installer package
* Additional mapping features
* Enhanced signal analysis tools

---

## Credits

Inspired and Mentored by Jeff W4DD

Created and Published by Mike KA4CDN

Modified by Eduardo N4EAC

---

## Disclaimer

This software is provided as-is without warranty. Signal measurements and S-meter conversions may vary depending on radio model, receiver settings, operating mode, and environmental conditions. Users are encouraged to verify results independently when performing critical measurements.

