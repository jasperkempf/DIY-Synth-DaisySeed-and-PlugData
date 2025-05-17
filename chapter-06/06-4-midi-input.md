---
layout: default
title: 06.4 MIDI-Input
parent: 06 Daisy Hardware Configuration
nav_order: 4
---

# 06.4 MIDI-Input

### 📥 Download all example Patches <a href="{{ site.baseurl }}/assets/diy-synth-example-files.zip" download>here</a> !
> 📖 The example files for this chapter are `MIDI-Input.fzz` and `JsonExample-Controls-MIDI-LEDS.json`.

## 🔌 MIDI-Input

To make our synthesizer **compatible with external devices** such as keyboards or sequencers, we will implement a **MIDI-Input.** This can be realized via the `UART Rx`-Pin, which is **Pin 14** on the Daisy. In order to make it work, we need to **convert the analog input** – that our MIDI-Port receives, **into serial data.** I am following the official MIDI-Documentation to install the MIDI-Input, which includes the following schematic:

<img width="1080" alt="midi-input-schematic" src="https://github.com/user-attachments/assets/d785da1d-aa7e-48a8-835e-e78809d0c248" />

> MIDI-Input installation according to the official MIDI-Documentation (https://drive.google.com/file/d/1L2YHBOZdSCuMg-RFR3TTEJcdV6KWkLZ9/view)

Converting the incoming data stream into serial data is achieved by **using an optocoupler** – in this case we’ll use the `6N138`, which is recommended in the official MIDI-Documentation above. The Schematic of the 6N138 giving us an insight of its functionality:

![Bildschirmfoto 2025-04-11 um 11 33 45](https://github.com/user-attachments/assets/d01f9375-99c4-42bc-a61f-b68634025dd9)
> 6N138 Schematic (Source: Reichelt)

The following **fritzing-schematic** shows, how I realized the connection on a breadboard to make the MIDI-input work. I used the following components:
- 1x 5-Pin DIN-Jack
- 1x 6N138 Optocoupler
- 1x 1N914 diode
- 1x 220Ω Resistor
- 1x 280Ω Resistor
- jumper wires

![midi-Input-fritz](https://github.com/user-attachments/assets/5c060f24-98d4-4f4e-9d54-9513c27857a5)

> 💡 Note that the analog and digital ground of the daisy are connected via the outer rail of the breadboard. This is recommended in the Daisy's Datasheet: https://daisy.audio/hardware/Seed/#technical-specs

In our **JSON-File**, we need to configure the MIDI-Input as follows:

```
  "defines": {
        "OOPSY_TARGET_HAS_MIDI_INPUT": 1
      },

```
→ This will activate MIDI-In and Output via the `UART-Rx` and `UART-Tx` Pins (Pin 13 and 14).

## 📦 PD MIDI-Objects

There are quite a few MIDI-related objects **that are compatible with heavy.** On the [hvcc Github repository by wasted audio](https://github.com/Wasted-Audio/hvcc/blob/develop/docs/04.midi.md), we can see the **full list of usable objects.** Using heavy, these objects will get replaced by “wrappers”, which route the incoming MIDI-Data to the right address.

> 💡 To ensure a **broad connectivity with many devices,** I will limit the usage of MIDI-Objects to the `notein`-object and implement **as many controls through hardware components as possible.** The example Patch Pd09-Polyphony.pd shows how MIDI is received via the `notein`-Object.

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 14 53 40" src="https://github.com/user-attachments/assets/9a17166b-3363-4e8b-802a-e0e974dbd09b" />

## → Continue with [flashing a patch]({{site.baseurl}}/chapter-07/07-flashing-a-patch)!
