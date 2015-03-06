---
layout: post
title: RF24USB Micro Pro board
---

RF24 Micro Pro board is a plug-in board as a base for Arduino Micro Pro. This Arduino is not that much known, but for some purposes it's cool.
Shortly: it has ATMega32u8 controller with USB support, similarly as Arduino Leonardo. You can find it in 5V/16MHz and 3.3V/8MHz variants.
It's a smallest Arduino I've seen, maybe together with Arduino Pro Mini. But unlike Pro Mini, one can upload firmware using bootloader there. And, the MCU supports USB, so it can be used for USB-related projects. And that's one of reasons why I've choosen that.

More details to the board: the idea is to make a small board with possibility to connect NRF modules. And when I say modules, I mean multiple of them :-)
So I there is possible to connect 2 modules simultaneously. Not only that, you can also choose whether to attach 8-pin or 10-pin NRF modules.
Modules are attached to SPI as usual, and pins CE, CSN and IRQ are attached to separate pins for each radio - see schematics. Usage of twin radios - this is a bit bookmark for future. Maybe one can try to use dual-head configuration with RF24Network.

Additional notes to the design:
* 3v3 regulator - Arduino Micro Pro does not have one, so I had to add it
* 10uF capacitor for radio power/ground stabilizing
* jumper to bypass 3v3 regulator. This is for the case 3v3 Arduino Micro Pro is attached
* FTDI header
* ICSP header
* there are couple of connectors for all Arduino pins so they can be further used

Schematics:
![RF24 Micro Pro schematics]({{ site.url }}/assets/rf24_micro_pro/rf24_micro_pro_scheme.png "RF24 micro pro scheme")

PCB:
![RF24 Micro Pro PCB]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_PCB.png "RF24 Micro Pro PCB")

PCB after de-panelizing:
![RF24 Micro Pro PCB photo]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_pcb.jpg "RF24 Micro Pro PCB photo")

The board after soldering of all components:
![RF24 Micro Pro empty]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_empty.jpg "RF24 Micro Pro empty")

With Arduino and one NRF module attached:
![RF24 Micro Pro 1]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_1.jpg "RF24 Micro Pro 1")

... connected to USB cable:
![RF24 Micro Pro 2]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_2.jpg "RF24 Micro Pro 2")

... and with 2 10-pin NRF modules:
![RF24 Micro Pro Dual]({{ site.url }}/assets/rf24_micro_pro/RF24_Micro_Pro_dual.jpg "RF24 Micro Pro Dual")

There are 2 bugs on the PCB:
1. wrong regulator pinout (as on all my boards from this batch
2. there was too thin trace on the edge of PCB between 2 NRF sections with +3v3. So I had to solder a short green wire to fix this.

Just to know for the case I want to do an additional order :-)

