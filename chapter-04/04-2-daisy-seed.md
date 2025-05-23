---
layout: default
title: 04.2 Daisy Seed
parent: 04 Tools
nav_order: 2
---

# 04.2 Daisy Seed

## 🌼 Daisy Seed

Let’s dive deeper into the heart of our project **– the Daisy Seed Microcontroller**. As mentioned before, it has been designed specifically for the creation of **embedded audio projects**. If you’ve never worked with a microcontroller before, you can imagine it as a controller **with a number of inputs and outputs** and a **processing unit in between**, that can interpret the input and send signals out through the outputs. We will take a detailed look at all the Pins below.

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 12 26 58" src="https://github.com/user-attachments/assets/5dfea2b1-fe7c-4442-89cc-7ae3963076c3" />

Let’s take a quick look at the overall specs of the Daisy Seed and why it is so well suited for audio projects. Firstly, it allows to be programmed in a number of languages such as **C++, Max gen~ and Pure Data, as well as Arduino**. This allows creators from different backgrounds and levels of experience to get started with their first Daisy-based projects. The Daisy runs on an **ARM Cortex-M7 MCU**, which is a **relatively high performing and energy efficient processor**. It allows for **stereo audio at 96kHz and 24-Bit**, enabling us to build **high fidelity audio devices.** With the 64MB version, you get 64MB SDRAM which can be used for storing **up to 10 minute long buffers.** Also it includes **8MB of external flash storage.**
It even features the opportunity of an SD card interface, PWM outputs and various serial protocols for external devices. You can learn more about the technical specifications of the Daisy Seed [here](https://daisy.audio/hardware/Seed/).

## 📌 Daisy Pin IO

We can roughly divide the pins in two categories – **analog (ADC) and digital** – which handle **different kinds of inputs** and can be used for different purposes. 

We have a total number of 40 Pins, of which we have **12x Analog Inputs** (A0-A11 / Pins 22-32 & Pin 35), **2x DAC outputs for Stereo-Audio** (Pins 18 & 19) and **2x ADC (Pins 16 & 17) for stereo-audio input.** 31 of the 40 total pins can be used as **digital pins, namely the pins 1-15** (D0-D14) and 22-37 (D15-D30).

Note that **one analog pin** can only be used for a **single control with a simple connection.** In this project, we will make use of **all 12 analog inputs.** If your project requires **additional analog controls**, you can use a **multiplexer to read out multiple signals via one analog input**, by making use of digital pins to “route” the signal to different destinations. You can read more about using a Multiplexer in [this article](https://electro-smith.com/blogs/seeds-n-circuits/what-the-mux-a-guided-tutorial-for-using-multiplexers-with-daisy).

![Daisy_Seed_Pinout](https://github.com/user-attachments/assets/cdad4d97-df48-4076-8c66-2dbf0820fe81)


The Pins referenced as **“peripheral GPIO”** (violet color) can be used to communicate with external devices and to send or receive serial data. In this project, we will only make use of the **UART4 Rx Input** (Pin 12 / D11) **to receive our MIDI-Input** from an outside source. However, if you plan on extending your project and want to **incorporate a display, SD-Card or other features**, I recommend reading more about the Daisy Pin IO [here](https://daisy.audio/hardware/Seed/). Note that not all features might be compatible with heavy and Plug Data.

## 💡 Daisy Memory 
The Daisy features a **few different types of internal memory**, differing in size and speed. The **internal flash-memory of 128kB** can be used to run smaller programs. If your Program exceeds this size, you need to flash the **bootloader** into the flash-memory and **upload the program into a different memory**, such as `SRAM`. The bootloader is a small program, that will boot our loaded program from other directories than the internal flash. This may sound complicated at first, but **it is easily done via the heavy-compiler integration in Plug Data**, where you simply select the size of your patch and it will get automatically assigned to the right memory storage of the daisy. We will have a detailed look at this in [chapter 07]({{site.baseurl}}/chapter-07/07-flashing-a-patch)

## → Continue with the next chapter about the heavy compiler [here]({{site.baseurl}}/chapter-04/04-3-hvcc)!
