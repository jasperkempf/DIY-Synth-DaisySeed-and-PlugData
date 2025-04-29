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
