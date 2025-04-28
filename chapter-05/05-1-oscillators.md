---
layout: default
title: 05.1 - Oscillators
parent: 05 - Programming a Synthesizer
nav_order: 1
---

# 05.1 - Oscillators

#### The example patches for this chapter are Pd01-oscillators and Pd02-counter. You can download all example patches <a href="{{ site.baseurl }}/assets/pd-patches/pd-examples.zip" download>here</a>


As a basis for our synthesizer, we need a sound source. In this chapter we will have a look at creating different types of oscillators, so we can switch between them for different sound characteristics. We will implement **the typical basic waveforms of Sine-, Saw,- and Square-wave**, as well as a **noise generator**.

To create an oscillator, we can choose between the pd Vanilla objects of `osc~` and `phasor` as well as the heavylib-generator `hv.osc~`. The `hv.osc~` can be configured as `hv.osc~ sine`, `hv.osc~ square`, `hv.osc~ saw` for generating different waveforms. As a noise source, the `hv.pinknoise`-object can be used. The Patch `Pd01-Oscillators` shows an example of these available generators and lets us listen to them by clicking on the message boxes in upper region of the patch. The patch also includes a Pitch and a Volume slider, which is connected to the most right inlet of the subpatch containing our generators.

![05-01-oscillators-patch](https://github.com/user-attachments/assets/2e227934-0e4a-4f8a-becc-e837ce166327)

By opening the `pd`-subpatch we can have a look at the internal mechanism, that lets us choose the different waveforms. Basically all sound generators are active at all times, but selecting one via the message boxes in the main patch will activate only one of them via the `route`-object, while deactivating all other sound sources. Activating and deactivating is done by a simple signal-multiplication. Multiplicating by 0 will mute the output, while multiplicating with a positive value – in this case 0.5 – will make it audible.

![05-01-Osc-Subpatch](https://github.com/user-attachments/assets/19bd2b11-c6ed-4bd1-aab0-ee7e730c714c)

As my instrument will work with simple controls only, i wanted to implement the functionality of switching through the waveforms by pressing a simple on/off-switch. Each time it's pressed, it should switch to the next waveform and begin from the first waveform again, once the last one is reached. To do that, i needed some sort of counter-mechanism, that would count every time the button is pressed and resets itself to 0 after a certain number of activations. As the `counter`-object is not compatible with heavy, i programmed a simple patch using the `%`-Operator (spoken: Modulo-Operator). 

The Modulo-Operator will give out the remainder of dividing the input with the output, using integers only. That means, a `% 4`-Operator will let all numbers from 0 to 3 through and reset to 0 when a 4 is reached (4/4 is 1, leaving a remainder of 0). Feeding the ouput of the `% 4`-operator into a variable message box `$ 1`, will replace the stored number. Each time the button is pressed, a `1` is send into the `+ `-operator, adding one to the stored number in the `$1`-variable. This now counts from 0 to 3, one step per button-press. To shift the range to 1 to 4 we simply add a `+ 1` operation on the output, which feeds into the `select 1 2 3 4`-object. This allows us to select multiple waveforms by pressing a simple button.

![05-01-counter](https://github.com/user-attachments/assets/59a1d1f0-c0f6-4e5b-a75d-9eba8d5d08e8)
