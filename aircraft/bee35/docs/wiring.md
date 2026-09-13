# Wiring

Port map, solder notes and jumper settings. **All assignments are TBC** until
confirmed against the MicoAir743 V2 pinout with hardware in hand.

## Port map

| Peripheral | Protocol | FC port | Pads | Notes |
|---|---|---|---|---|
| RadioMaster RP3 V2 | CRSF | UART TBC | RX/TX | |
| Flywoo GM10 Mini V3 (GPS) | UBX | UART TBC | RX/TX | |
| Flywoo GM10 Mini V3 (compass) | I2C | I2C TBC | SCL/SDA | FC internal compass disabled, see [`setup-inav.md`](setup-inav.md) |
| MicoAir MTF-01P | MSP | UART TBC | RX/TX | MSP mode set via solder jumper on the sensor |
| Walksnail Avatar VTX | MSP DisplayPort | HD VTX connector | | Usually default |
| Camera tilt servo (optional) | PWM | Spare output S5+ | | Reserved. Verify the board exposes usable servo outputs in multirotor configuration first |

## Solder notes

TBC. Record pad locations, wire gauges, and anything non-obvious about the physical
build here as it is done.

## Jumper settings

TBC. Record the MTF-01P MSP jumper state and any FC jumpers here.

## Power

XT60 pigtail and 35 V 470–1000 µF low-ESR capacitor on the ESC input. Check the
stack box contents before ordering.
