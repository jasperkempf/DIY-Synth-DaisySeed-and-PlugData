---
layout: default
title: 04.4 JSON File
parent: 04 Tools
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

This is what my final JSON-File looked like, where i included 12 analog controls, 6 Switches and 6 LEDs:

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
        },
        "p2": {
            "component": "AnalogControl",
            "pin": 16
        
        },
        "p3": {
            "component": "AnalogControl",
            "pin": 17
        
        },
        "p4": {
            "component": "AnalogControl",
            "pin": 18
        
        },
        "p5": {
            "component": "AnalogControl",
            "pin": 19
        
        },
        "p6": {
            "component": "AnalogControl",
            "pin": 20
        
        },
        "p7": {
            "component": "AnalogControl",
            "pin": 21

        
        },
        "p8": {
            "component": "AnalogControl",
            "pin": 22
            
        
        },
        "p9": {
            "component": "AnalogControl",
            "pin": 23
            
        
        },
        "p10": {
            "component": "AnalogControl",
            "pin": 24
            
        
        },
        "p11": {
            "component": "AnalogControl",
            "pin": 25
            
        
        },
        "p12": {
            "component": "AnalogControl",
            "pin": 28
            
        
        },

        "led1": {
            "component": "Led",
            "pin": 12
        },

        "led2": {
            "component": "Led",
            "pin": 11
        
        },

        "led3": {
            "component": "Led",
            "pin": 10
        
        },

        "led4": {
            "component": "Led",
            "pin": 9
        
        },

        "led5": {
            "component": "Led",
            "pin": 8
        
        },

        "led6": {
            "component": "Led",
            "pin": 7
        
        },

   

        "sw1" : {
            "component": "Switch",
            "pin": 0
        },

        "sw2" : {
            "component": "Switch",
            "pin": 1
        },

        "sw3" : {
            "component": "Switch",
            "pin": 2
        },

        "sw4" : {
            "component": "Switch",
            "pin": 3
        },

        "sw5" : {
            "component": "Switch",
            "pin": 4
        },

        "sw6" : {
            "component": "Switch",
            "pin": 5
        }
        
      
        
        
    }
}


```
