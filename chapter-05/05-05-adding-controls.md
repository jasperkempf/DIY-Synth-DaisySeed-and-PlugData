---
layout: default
title: 05.5 - Adding Controls
parent: 05 - Programming a Synthesizer
nav_order: 5
---

# 05.5 - Adding Controls

As we ultimately want to control our Synthesizer with hardware components via our microcontroller, we need to configure the Plug Data patch accordingly. While we're looking at setting up controls on the hardware side in chapter 06, i want to cover the software aspects in this chapter. Here i want to give a few tips on what to look out for, especially when using analog controls like potentiometers. 

## Sliders vs. Analog Inputs (_Pd11-sliders-vs-analog.pd_)

When using slider objects, to mimic our analog input while patching, it is very important to know that they don't exactly work alike. There is one crucial difference, that can cause unexpected behaviour if ignored: 

**The analog input will cause a permanent data stream and a constant transmission of Data into the program, while a slider only transmits a value when the control is used!**

This is important to know, as some objects trigger a calculation once they receive data on their left input. If you expect the calculation to happen only, if the slider is moved, it will behave differently when controlled by an analog control – causing an uninterrupted series of calculations. However, we can "simulate" this behaviour by using something like a `metro 2`-object to trigger the calculations continuosly while we're patching.  The Patch _Pd11-sliders-vs-analog.pd_ shows an example of both cases. 

<img width="540" alt="Bildschirmfoto 2025-05-01 um 11 39 06" src="https://github.com/user-attachments/assets/a784dec3-f9e5-40f8-b011-b804f4b73e35" />
