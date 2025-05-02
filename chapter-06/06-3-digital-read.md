---
layout: default
title: 06.3 Digital Pin Values (Switch, LED)
parent: 06 - Daisy Hardware Configuration
nav_order: 3
---

# 06.3 Digital Pin Values 

Now that we know how to add analog controls, **let’s look at reading and sending digital signals.** As opposed to analog inputs – which can read out “floating” analog values and convert them to float-numbers between 0 and 1 – **A digital Input only knows two states: High and low voltage.** Depending which one is the case, this corresponds to a **digital read-out value of 1 (“high”) or 0 (“low”).**

In this example **we will install a simple switch (“on/off-button”)** and use it to **turn an LED on or off**, which is connected to a second digital Pin.

Similar to our analog input, we use the same `@hv_param`-flag to create **receive (“r” = input) or send-object (“s” = output)** in Plug Data. A digital input named `sw1` could be declared like this:

<img width="270" alt="swiitch" src="https://github.com/user-attachments/assets/6a5e72a9-a059-46d4-bae0-819bc3d9858b" />

Note how there is no difference to the analog input noticeable yet. **Pd will simply receive the input and route it to its destination.** However, we need to tell the Daisy Seed, **which input the parameter `sw1` needs to be read out from.** This happens again in our JSON-File as follows:

```
 "sw1" : {
            "component": "Switch",
            "pin": 0
        },
```

As we flash our patch together with our custom JSON-File onto the Daisy, it will “understand” that the **Parameters declared in Pd correspond to the Pins named in the JSON-File.**
In this case we declared a `Switch`-component and connected it to Pin 0 (“D0”) – **which is a digital Pin on the Daisy.** 

Now we can reverse to whole process and **create a digital outlet by using a send-object `s` **. The send-object is created similar to the receive-object. Here I created a send-object called `led1`.

<img width="270" alt="led-pd" src="https://github.com/user-attachments/assets/2a81fae5-5702-4cc2-a802-47c5583427ef" />

In our JSON-File, I declare `led1` as an Led-component  and connect it to Pin 12 (D12). The Daisy will then pass on the values from the patch as high or low voltage and send it out via the digital Pin 12.

```
   "led1": {
            "component": "Led",
            "pin": 12
        },
```
<img width="270" alt="led-json" src="https://github.com/user-attachments/assets/a584ffde-20b3-484f-bdfa-0b6057c1d38d" />

Now we can connect our switch and the LED components to our Daisy as seen in the following schematic. The analog and digital ground of the Daisy are connected via the outer rails and **to protect the LED, a 470Ω resistor is used.**

![swled-fritz](https://github.com/user-attachments/assets/606d7513-4413-4210-b961-40a3255e8aea)


Instead of a switch, you could use **a button or other electronic components, which will be connected similarly.** If you’re unsure how to connect your specific component, **you can always look up the schematic of your component to understand how it works.**

