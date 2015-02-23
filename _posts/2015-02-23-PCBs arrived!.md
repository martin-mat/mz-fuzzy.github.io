---
layout: post
title: PCBs arrived!
---

Recently I've spend my free time working on [RF24Remote](https://github.com/mz-fuzzy/RF24Remote). It's a library for remote driving of nRF24l01 cheap radio boards using well-known [RF24 library](https://github.com/TMRh20/RF24). The software part seems to be working (however it still needs some fine tuning), and I reached also some progress on HW part of the project. Designed boards vi GEDA (easy), routed them in GEDA pcb (damn hard). Panelized and sent to [DirtyPBC](http://dirtypcbs.com/) to make set of 10x10cm PCBs. Cost $25 - good price especially considering possible panelizing. It took some time to deliver it, but today they are here!

![Panelized PCBs]({{ site.url }}/assets/Panelized_PCBs_RF24Remote.jpg "Panelized PCBs")

Some points:
* They announce that the number of boards are 8-12. For me it was 10.
* Looking closer to PCB quality, they are really kind of 'dirty'. But it seems that they are ok from functinality point of view.
* They came untracked. Postman left it at my neighbor. I'm wondering what would happen if it get lost somewhere during transport. I doubt that DirtyPCBs would re-make and re-send. Do you anyone have experience from such case? If so feel free to comment below.

Depanelizing went quite ok. I have never designed boards with panelizing, but it went fine. No problems with board breaking, just used pliers. After that I sanded boards a bit.

I already started soldering of the first board - RF24VUsb Mini. I'll write a separate post about that. What I can write already now is that I made 2 flaws to design. Bad point is that flaws hit almost all boards. Good is that they are not fatal:
* for USB-A I used a footprint which I found somewhere on internet. Unfortunately pins are mirrored. My bad, I should have checked it. This is easily fixable by soldering if the USB connector to the other side. Not a big deal.
* I used bad pinout for 3.3V regulator. Input and output are reversed. For fixing this I needed to be a bit more creative when soldering the regulator. But finally also success.

Hopefully I'll not discover any other errors. It's basically by second board ordered, so I'm still collecting experiences. Next time I hope no such stupid bugs!


