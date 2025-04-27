---
layout: default
title: 04.4 - JSON File
parent: 04 - Tools
nav_order: 4
---

# 04.4 - JSON File

A JSON-File (Javascript object notation) is a text-based code-file to store and transmit data. It is relatively simple and easy to read. We will use it, to tell the Daisy Seed, which Inputs and Outputs – which we configured in our Plug Data Patch – correspond to which pins of the microcontroller. The JSON-File will function as the connection between hardware and software and is crucial for our Instrument to work properly. 

We will configure all used potentiometers, switches, leds as well as the number of our audio-channels and the MIDI-functionalities in this file. To upload it to our Daisy, we can select the file in the compile-window inside Plug Data when flashing our patch.

This is what a simple JSON-File could look like to configure one potentiometer, MIDI and stereo-audio.

```
{
    "name": "customseed",
    "som": "seed",

    "audio": {
        "channels": 2
    },

   "defines": {
        "OOPSY_TARGET_HAS_MIDI_INPUT": 1
      },

  "components": {
        "p1": {
            "component": "AnalogControl",
            "pin": 15
              }
          }
}
```

There are a few more examples and further resources about building custom JSON-files for Daisy available on the [Daisy support site](https://daisy.audio/tutorials/oopsy/oopsy-custom-json/) as well as in the [Oopsy Github repository](https://github.com/CorvusPrudens/oopsy/tree/sensors_update/source)
