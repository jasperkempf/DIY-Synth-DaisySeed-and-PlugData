---
layout: default
title: 06.1 Audio IO
parent: 06 Daisy Hardware Configuration
nav_order: 1
---

# 06.1 Audio IO

### 📥 Download all example Patches <a href="{{ site.baseurl }}/assets/diy-synth-example-files.zip" download>here</a> !
> 📖 The example files for this chapter are `Audio-In.fzz`, `Audio-In.fzz` and `JsonExample-Controls-MIDI-LEDS.json`.

## 🔊 Audio IO

Installing and Audio-In and Output is quite simple with the Daisy. We will use the `Pins 18` and `19` (Audio Out 1&2) for installing a stereo output jack. Vice versa, the `Pins 16 & 17` can be used to install a **stereo input**. The following schematic shows **two variants of stereo jacks** and how they are connected. 

> 💡 You would **only need one of the two jacks for a stereo output** (Note that the jacks need to be **stereo components**). If you want to install a **mono jack**, simply **connect only one of the output- (or input) Pins** of the Daisy to the Tip-Connector and the Sleeve-Connector of the jack to ground.

![daisy-output](https://github.com/user-attachments/assets/df8aa7e4-3f6c-4473-8cf3-afe06d2cd405)

Installing an audio input is very similar and simply requires us to connect the `input pins (16 & 17) ` of the Daisy to our stereo jack as seen here:

![input](https://github.com/user-attachments/assets/2805afaf-daa3-41de-94f8-77d5480e4f81)

In Pd **our Output is declared by creating a** `dac~`-Object (digital to analog converter), an input is created via the `adc~`-Object

<img width="540" alt="adcdac" src="https://github.com/user-attachments/assets/7ff89289-6b11-4387-8457-a90b1d99d014" />

In our JSON-File, **we declare two audio channels** with the following code:

```
   "audio": {
        "channels": 2
    },
```

Now we can run a Pd-Patch on the Daisy that will output the signal from the patch via the Output-Pins of the Microcontroller.

Let's continue with the next chapter on [reading analog pin values]({{site.baseurl}}/chapter-06/06-2-analog-read)
