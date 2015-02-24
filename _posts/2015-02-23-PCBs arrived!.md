---
layout: post
title: PCBs arrived!
---

Recently I've spend my free time working on [RF24Remote](https://github.com/mz-fuzzy/RF24Remote). It's a library for remote driving of nRF24l01 cheap radio boards using well-known [RF24 library](https://github.com/TMRh20/RF24). The software part seems to be working (however it still needs some fine tuning), and I reached also some progress on HW part of the project. Designed boards vi GEDA (easy), routed them in GEDA pcb (damn hard). Panelized and sent to [DirtyPBC](http://dirtypcbs.com/) to make set of 10x10cm PCBs. Cost $25 - good price especially considering possible panelizing. It took some time to deliver it, but today they are here!

![Panelized PCBs]({{ site.url }}/assets/Panelized_PCBs_RF24Remote.jpg "Panelized PCBs")

Boards there:

1. RF24VUSB 0.9z: Basic board for RF24Remote with VUSB. Uses VUSB variant with level conversion using zener diodes. Utilizes ATMega328p on 5V/20MHz. Double nRF24l01 headers, both 8 and 10 pin sockets. 3 LEDs. ICSP, FTDI headers, plus additional header with some GPIO pins. Reset button and one additional button intended for FW flash initiation via VUSB.
2. RF24VUSB 0.9: same as (1.) except of VUSB connection - supply voltage is reduced to 3.3V. Crystal expected to be 12MHz.
3. RF24USB 0.9: RF24Remote with ATMega32u4. Library for this does not exist yet, but is planned. Also planned to be used for a Ethernet USB card with [RF24Ethernet](http://tmrh20.github.io/RF24Ethernet/).
4. RF24VUSB Mini: minimized variant of (2.) with no buttons, one LED, one 8-pin nRF24l01 header.
5. RF24USB Micro Pro: shield for Arduino Micro Pro (with ATMega32u4). Similar as (3.) but the arduino is used as the core.
6. Bread Helper board: a helper for my breadboard prototyping. Micro usb for power and VUSB connections, 2 buttons, 2 LEDs, 3.3V/5V select, crustal socket.
7. nRF24l01 convertor: converts 10-pin nRF24l01 modules to 8-pin socket + adds capacitor.

Some points to the boards:

* DirtyPCBs announce that the number of boards are 8-12. For me it was 10.
* Looking closer to PCB quality, they are really kind of 'dirty'. But it seems that they are ok from functinality point of view.
* They came untracked. Postman left it at my neighbor. I'm wondering what would happen if it get lost somewhere during transport. I doubt that DirtyPCBs would re-make and re-send. Do you anyone have experience from such case? If so feel free to comment below.

Depanelizing went quite ok. I have never designed boards with panelizing, but it went fine. No problems with board breaking, just used pliers. After that I sanded boards a bit.

I already started soldering of the first board - RF24VUsb Mini. I'll write a separate post about that, for now just a picture:
![RF24VUSB mini]({{ site.url }}/assets/RF24VUSB_mini.jpg "RF24VUSB mini")

What I can write already now is that I made 2 flaws to design. Bad point is that flaws hit almost all boards. Good is that they are not fatal:

* for USB-A I used a footprint which I found somewhere on internet. Unfortunately pins are mirrored. My bad, I should have checked it. This is easily fixable by soldering if the USB connector to the other side. Not a big deal.
* I used bad pinout for 3.3V regulator. Input and output are reversed. For fixing this I needed to be a bit more creative when soldering the regulator. But finally also success.

Hopefully I'll not discover any other errors. It's basically by second board ordered, so I'm still collecting experiences. Next time I hope no such stupid bugs!


