---
layout: default
title: 03 Components
nav_order: 4
---

# 03 Components
For this Project, we’re going to need a list of components to bring our Instrument to life.

## Daisy Seed Microcontroller
Firstly and most importantly we need the heart and brain of our instrument – **the Daisy Seed Microcontroller**. This is a microcontroller which has been designed specifically for the creation of **embedded audio projects**. It is quite affordable and programmable with a variety of programming languages such as **C++, Max gen~** and **Pure Data / Plug Data**. You can buy the Daisy Seed in the official webshop [here](https://electro-smith.com/products/daisy-seed) or try to find a local electronics dealer in your area which might have them in stock (which could potentially minimize shipping costs and delivery times). 
We will dive deeper into the capabilities of this microcontroller in this chapter (link). To power the microcontroller and to load our patch onto it, we need a **micro-usb cable**. Make sure **it can transmit data**, as some micro-usb cables are only for charging devices and not for transmitting data. (Note that this cable is not included with the Daisy Seed upon delivery!)
<img width="540" alt="Bildschirmfoto 2025-05-15 um 12 26 58" src="https://github.com/user-attachments/assets/d45c6ab1-5106-4fff-8385-8c3faf9b1238" />

## Control elements (switch, Potentiometers)
To control parameters of our instrument, we will be using **potentiometers** **and switches**. Additionally, we can use **LEDs** to indicate different states of our Instrument or to give some sort of visual feedback when changing parameters. These componenets are usually **quite affordable and easy to install**, which we will cover in this chapter (link).

## Prototyping electronics (Breadboard, Jumper wires, resistors)
Furthermore, building our first prototype will require some additional parts such as a **breadboard**, **jumper wires and some resistors** with different impedances to build our circuit and to make sure certain components – such as our LEDs – are **protected from damage**.

## MIDI Components 
Thirdly we will need some specific components to install **a MIDI-Port**. In this Project, we will learn how to install a **5-Pin MIDI-Input** to our Daisy Seed, so we require a 5-Pin DIN-Jack, as well as a 5-Pin Midi-cable for that. To transform our incoming Midi-signal into serial-data, we will need a **6N138 Optocoupler** and a simple **1N914 diode** to protect our circuit. 

## Audio-Jack
Last but not least: **We need an Audio-output!** I have chosen a **6,3mm Stereo-Jack** and the fitting cable for this project. You could also use a **3,5mm stereo- or mono-jack**, depending on your project. If you plan installing an Audio-Input – for example for building an effect-pedal– **you will need to install a second jack for that.**

## List of components:

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
- 

**Audio :**
- 6,3mm Stereo-Jack
- 6,3mm Stereo-cable
