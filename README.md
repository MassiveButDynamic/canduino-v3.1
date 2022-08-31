# CANdunio v3

Here you can find a tutorial how to get started with your CANduino `v3.1`. Please make sure that you really use the `v3.1`, because on `v3` the CS_Pin was `CS_Pin 8`!

## Getting started

Before we can start with the program it is important to check if the jumper `CAN_CS` (on top next to the USB-C port) is connected to a soldering point. Only if this is connected, it is possible to address the mcp2515.

The following library must be installed before use: https://github.com/autowp/arduino-mcp2515/archive/master.zip

If your CANduino is at the end of the CANbus chain, it is mandatory to connect the CAN_T jumper (next to the CAN connector)!

## Important parameters

So that the mcp2515 can be addressed it is important to set the following parameters:
```
MCP2515 mcp2515(10);
mcp2515.setBitrate("Your Bitrate", MCP_8MHZ);
```

## Example Code

In the `examples` folder you will find two code examples with which you have the possibility to `send` and `receive` CAN messages.

## Troubleshooting

If the CANduino is not displayed, please download the driver for the CH340 which can be found here: http://www.wch-ic.com/downloads/CH341SER_ZIP.html

If you have the `CANduino v3 with ATmega168PA` the following board manager URL must be inserted in the programming environment (Arduino IDE). The bootloader is preinstalled: https://mcudude.github.io/MiniCore/package_MCUdude_MiniCore_index.json

Please use our instructions for v3 which you can find here: https://github.com/MassiveButDynamic/canduino-v3

## Pinout

Here you can find a pinout of the CANduino v3:
![Pinout](/Pinout-CANduinov3.1.png)
