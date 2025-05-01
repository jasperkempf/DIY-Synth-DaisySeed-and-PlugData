---
layout: default
title: 05.5 - Adding Controls
parent: 05 - Programming a Synthesizer
nav_order: 5
---

# 05.5 - Adding Controls

As we ultimately want to control our Synthesizer with hardware components via our microcontroller, we need to configure the Plug Data patch accordingly. While we're looking at setting up controls on the hardware side in chapter 06, i want to cover the software aspects in this chapter. Here i want to give a few tips on what to look out for, especially when using analog controls like potentiometers. 

## Simulating Controls (_Pd11-simulating-analog_smoothing.pd_)

While programming our synth, we need to know if the incoming values – which the Daisy will receive from hardware components – are distributed correctly in the patch and produce the desired results. To simulate hardware controls for simple testing while patching, i use horizontal slider objects `hsl`. As the expected input from analog controls moves between 0 and 1 by default, I've set the range of the sliders to these same values. You can also define a specific range in heavy-parameter-bjects, by including minimum and maximum values:  `r p1 @hv_param 200 2000`. However, i found keeping the range of the controls between 0 and 1 and then expanding the range with simple multiplications sufficient.

## Sliders vs. Analog Inputs (_Pd12-sliders-vs-analog.pd_)

When using slider objects, to mimic our analog input while patching, it is very important to know that they don't exactly work alike. There is one crucial difference, that can cause unexpected behaviour if ignored: 

**The analog input will cause a permanent data stream and a constant transmission of Data into the program, while a slider only transmits a value when the control is used!**

This is important to know, as some objects trigger a calculation once they receive data on their left input. If you expect the calculation to happen only, if the slider is moved, it will behave differently when controlled by an analog control – causing an uninterrupted series of calculations. However, we can "simulate" this behaviour by using something like a `metro 2`-object to trigger the calculations continuosly while we're patching.  The Patch _Pd11-sliders-vs-analog.pd_ shows an example of both cases. 

<img width="540" alt="Bildschirmfoto 2025-05-01 um 11 39 06" src="https://github.com/user-attachments/assets/a784dec3-f9e5-40f8-b011-b804f4b73e35" />

If your program does not work as expected once it's flashed on the Daisy, this could be something to look out for.

## Smoothing

Because of the slight variation of input voltage, which is received through the analog inputs, it is recommmended to apply a certain amount of smoothing. This can be done via a `line`-object and a `$1 10`-message box.

