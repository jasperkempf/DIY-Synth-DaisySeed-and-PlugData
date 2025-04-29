---
layout: default
title: 05.3 - Modulation
parent: 05 - Programming a Synthesizer
nav_order: 3
---

# 05.3 - Modulation

### The example patches for this chapter are _Pd04-LFO-Example_ and _Pd05-Envelopes_.

You can download all example patches <a href="{{ site.baseurl }}/assets/pd-patches/pd-examples.zip" download>here</a>

To expand the sound design possibilities of our Instrument, we'll have a look at implementing two different types of modulation – LFOs (low frequency oscillators) and Envelopes. Both can technically be used to modulate any thinkable parameter of a synth. While LFOs describe a modulation curve, that is running permanently (unless configured otherwise) at the set Rate or frequency, an envelope is typically triggered by incoming note-on and note-off events (typically transmitted through MIDI-Data).

## LFOs

Our example Patch _Pd04-LFO-Example_ is a simple patch, that lets us select different LFO-waveshapes and visualizes them for demonstrative purposes. Changing the waveform via the Toggle and altering the Frequency via the slider gives us a better understanding of the underlying signal generation that is taking place in the subpatch.

<img width="1080" alt="05-03-LfoExample" src="https://github.com/user-attachments/assets/e3ecee31-24da-4b6e-b277-1bde53ae20ff" />
