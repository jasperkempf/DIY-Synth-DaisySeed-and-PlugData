---
layout: default
title: 06.2 Reading Analog Pin Values (Potentiometer)
parent: 06 Daisy Hardware Configuration
nav_order: 2
---

# 06.2 Reading Analog Pin Values 

### 📥 Download all example Patches <a href="{{ site.baseurl }}/assets/diy-synth-example-files.zip" download>here</a> !
> 📖 The example files for this chapter are `Potentiometer-Example.fzz` and `JsonExample-Controls-MIDI-LEDS.json`.

Let’s have a look at **reading analog pin values from a potentiometer**. In the example patch, you will see an external input declared as a heavy parameter. For Heavy-Parameters, we use the flag `@hv_param` to define a parameter. The letter “r” declares it as receive object, opposed to “s” which would create a an output as a send-object.

In order to receive a signal from an analog pin, **we need to tell the Daisy Seed, which Pin the Parameter corresponds to**. This has to be declared in our custom JSON-File. The following screenshot shows an example and the respective code of how this can be configured for an input parameter called “p1” which will be read out from Pin 15, which is Pin A0 on the Daisy Seed. 

<img width="270" alt="input" src="https://github.com/user-attachments/assets/eef02f10-5313-4866-95b4-d8485b0319b1" />

```
"components": {
                "p1": {
                    "component": "AnalogControl",
                    "pin": 15
                }
        }
```

Now the last thing we need to do is to connect a potentiometer to our microcontroller. In the following schematic you can see how to connect the potentiometer to your breadboard and the Daisy Seed.

![poti-fritz](https://github.com/user-attachments/assets/53d25568-2a8c-45ed-93c4-d265de336029)


✅ And that’s already it! If you configured the parameter correctly in your JSON-File and your Pd-Patch, **you should now be able to receive values from the analog inputs into the flashed patch**. 

> 💡Note that it is only possible to receive the data when it is flashed on the Daisy, so you always need to flash it via the compiler onto the controller to see if it works out. I recommend building a simple patch – like the example patch for analog inputs – first, which controls a simple parameter like the pitch of an oscillator.

The analog input values are converted to digital values in a range of 0 to 1. If you want to expand that range, **just add a simple multiplier to the value** as follows:

<img width="1080" alt="example" src="https://github.com/user-attachments/assets/b179f544-0d93-4715-8f80-8afd1e64b37f" />

## → Let's continue with the next chapter on [reading digital pin values]({{site.baseurl}}/chapter-06/06-3-digital-read)!
