---
layout: default
title: 03 Components
nav_order: 4
---

# 03 Components
For this Project, we’re going to need a list of components to bring our Instrument to life.

## Daisy Seed Microcontroller

First and foremost, we need the heart and brain of our instrument — **the Daisy Seed microcontroller.**
This microcontroller was designed specifically for creating **embedded audio projects**. It’s relatively affordable and can be programmed using a variety of languages, including **C++, Max gen~, and Pure Data / Plug Data.** You can purchase the Daisy Seed from the official webshop [here](https://electro-smith.com/products/daisy-seed), or check with local electronics retailers in your area — they may have it in stock, which could help reduce shipping costs and delivery times.

> We’ll take a closer look at the **features and capabilities of this microcontroller** later in [this Chapter]({{site.baseurl}}/chapter-04/04-2-daisy-seed).

To power the Daisy Seed and upload your patch to it, **you will need a micro-USB cable.** Make sure the cable supports **data transfer,** as some micro-USB cables are designed for charging only and cannot transmit data.

⚠️ Note: A compatible USB cable is **not included with the Daisy Seed** when you order it!

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 12 26 58" src="https://github.com/user-attachments/assets/f3291f92-d62e-4e8c-9b30-425e941ea7a2" />


## Control elements (Switches, Potentiometers)
To control various parameters of our instrument, we will use **potentiometers and switches**. In addition, LEDs can be added to indicate **different states of the instrument** or provide visual feedback when parameters are adjusted. These components are generally **affordable and easy to install**. We will cover **how to work with them in more detail** later in [this Chapter]({{site.baseurl}}/chapter-06/06-Daisy-Hardware-Configuration).

![components-01](https://github.com/user-attachments/assets/28208144-f4b7-4db9-8ef3-3caf6e7b2eb0)

## Prototyping electronics (Breadboard, Jumper wires, resistors)

To build our first prototype, we’ll also need a few essential components: **a breadboard, jumper wires, and resistors of various values.** These parts are used to **assemble the circuit** and ensure that certain components — like LEDs — are **properly protected from damage**.

![components-02](https://github.com/user-attachments/assets/99074a28-9f5d-4aa5-ba31-fbdaf0c2964e)

## MIDI Components 
Thirdly we will need some specific components to install **a MIDI-Port**. In this Project, we will learn how to install a **5-Pin MIDI-Input** to our Daisy Seed, so we require a 5-Pin DIN-Jack, as well as a 5-Pin Midi-cable. **To transform our incoming MIDI-signal into serial-data**, we will need a **6N138 Optocoupler** and a simple **1N914 diode** to protect our circuit. 
![components-03](https://github.com/user-attachments/assets/5162c29c-d2ed-4fd8-b009-e4b5d7ccaecf)

## Audio-Jack
For this project, I’ve chosen a **6.3mm (¼ inch) stereo jack along with a matching cable.** However, you can also use a 3.5mm stereo or mono jack, depending on the needs of your setup. If you plan to include an audio input — for example, when building an **effect pedal** — you’ll need to install a second jack to handle that connection.
![components-04](https://github.com/user-attachments/assets/028e0d04-d3e7-42ed-bdc7-ce1f5d540a0d)


## 📝 List of components used in this project:

  **Microcontroller**:
  - Daisy Seed Microcontroller
  - Mini-USB Cable (Data Transmitting)
  
  **Control Elements and Prototyping:**
  - 12 x 10K Potentiometer
  - Breadboard-friendly switches
  - LEDs
  - Breadboard
  - Jumper wires
  - Resistors 470Ω (1x per used LED)
  
  
  **MIDI:**
  - 5-Pin DIN-Jack
  - 5-Pin Midi-cable
  - 6N138 Optocoupler
  - 1N914 diode
  - Resistors 220Ω
  - Resistors 280Ω
  
  **Audio :**
  - 6.3mm Stereo-Jack (alternatively 3.5mm mono, or stereo-jack)
  - 6.3mm Stereo-cable (3.5mm mono/ stereo cable)
  
  **Additional Tools :**
  - Soldering Station


## → Continue with Chapter 04 [here]({{site.baseurl}}/chapter-04/04-Tools)!
