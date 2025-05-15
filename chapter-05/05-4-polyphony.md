---
layout: default
title: 05.4 Polyphony
parent: 05 Programming a Synthesizer
nav_order: 4
---

# 05.4 - Polyphony 

> You can download all example patches <a href="{{ site.baseurl }}/assets/diy-synth-example-files.zip" download>here</a>

### Simple Polyphony (Pd09-Polyphony.pd)

To make our synthesizer capable of playing multiple notes at once, we will have a look at implementing Polyphony. The example patch _Pd09-Polyphony.pd_ shows how to implement 4 Voices of Polyphony.

In Plug Data, multiple vooices can be created using the `poly `-object. As we receive MIDI-Data via the `notein`-object or by activating the simple sequencer, we use a `pack f f` to pack the note number and the velocity into a list. The `poly 4` object assigns the incoming Note-Information to one of 4 voices. The output of the `poly 4` is packed by a `pack f f f`-object (Voice number, Note Number, Note Velocity) and then fed into a `route 1 2 3 4`-object. As the voice number marks the first position in the list created by `pack f f f`, the `route 1 2 3 4` will distribute each note and velocity-value out of it's corresponding outlet (Voice Number 1 -> Route output 1). 

Now we have 4 blocks of `unpack`-objects that split up the lists into pairs of note and velocity values again. The Note values are transformed into frequency-values by an `mtof`-object, and are passed onto a `pd oscillators`-subpatch, which contains our sound generators. Each voice has their own subpatch with the same set of generators inside.

<img width="540" alt="05-03-Polyphony" src="https://github.com/user-attachments/assets/fa5a7047-a06a-4373-96a9-8f0b66c745a5" />

In this example, the Velocity values are used to stop the notes from playing at a velocity of 0. They are routed into a `line~ `-object to create a simple ramp with a smoothing of 10ms via the `$1 10`-message.

### Polyphonic Envelopes (Pd10-Poly-Envelopes.pd)

To make our notes more natural-sounding than just a simple on-off signal, we can implement the Attack-release-envelope which we've created in the previous chapter. Each voice needs their own envelope, while all envelopes should receive the same attack and release values. The Patch _Pd10-Poly-Envelopes.pd_ shows how each voice features its own envelope.

<figure>
  <img width="540" alt="Bildschirmfoto 2025-04-29 um 17 47 34" src="https://github.com/user-attachments/assets/cf004b5c-dba0-41c1-8bf3-4608e0297276" />
  <figcaption> Implementation of polyphonic envelopes (Pd10-Poly-Envelopes.pd) </figcaption>
</figure>

Using send and receive objects, the attack and release values are passed on to each `pd AR Envelope`-subpatch from the controls on the top right of the patch. This also keeps the patch a bit more organized and less crowded.

Continue with the next chapter on adding controls [here]({{site.baseurl}}/chapter-05/05-05-adding-controls)!

