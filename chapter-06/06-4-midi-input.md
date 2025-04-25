---
layout: default
title: 06.4 MIDI-Input
parent: 06 - Daisy Hardware Configuration
nav_order: 4
---

# 06.4 MIDI-Input

To make our synthesizer **playable with external devices** such as keyboards or sequencers, we will implement a **MIDI-Input.** This can be realized via the `UART Rx`-Pin, which is **Pin 14** on the Daisy. In order to make it work, we need to c**onvert the analog input** – that our MIDI-Port receives, **into serial data.** This can be done by **using an optocoupler** – in this case we’ll use the 6N138, which is recommended in the official MIDI-Documentation. The MIDI-Documentation includes the following schematic:

<img width="454" alt="midi-input-schematic" src="https://github.com/user-attachments/assets/d785da1d-aa7e-48a8-835e-e78809d0c248" />

The following **fritzing-schematic** shows, how I realized the connection on a breadboard to make the MIDI-input work. I used the following components:
- 1x 5-Pin DIN-Jack
- 1x 6N138 Optocoupler
- 1x 1N914 diode
- 1x 220Ω Resistor
- 1x 280Ω Resistor

![midi-Input-fritz](https://github.com/user-attachments/assets/5c060f24-98d4-4f4e-9d54-9513c27857a5)

In our **JSON-File**, we need to configure the MIDI-Input as follows:

```
  "defines": {
        "OOPSY_TARGET_HAS_MIDI_INPUT": 1
      },

```
There are quite a few MIDI-related objects **that are compatible with heavy.** On the [hvcc Github repository by wasted audio](https://github.com/Wasted-Audio/hvcc/blob/develop/docs/04.midi.md), we can see the **full list of usable objects.** Using heavy, these objects will get replaced by “wrappers”, which route the incoming MIDI-Data to the right address.

To ensure a **broad connectivity with many devices,** I will limit the usage of MIDI-Objects to the `notein`-object and implement **as many controls through hardware components as possible.**
