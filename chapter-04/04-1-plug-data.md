---
layout: default
title: 04.1 Plug Data
parent: 04 Tools
nav_order: 1
---

# 04.1 Plug Data

## Plug Data

Plug Data is a visual programming environment for audio and multimedia applications, based on Pure Data Vanilla. We have already mentioned some of the benefits of Plug Data in the [Installations Chapter]({{site.baseurl}}/chapter-02/02-Installations). However, I want to take a moment to dive a little deeper into the capabilities of this program and **point out certain features that make it a really good tool** for our first project.

Firstly, as the software is **open source, Plug Data is completely free to download**. As it is based on Pure Data Vanilla, **a lot of tutorials exist** in the web and Pure Data patches are **fully compatible with Plug Data** (and vice versa), which means there are many great resources for beginners to get started. The **visual programming environment** is also much more **beginner-friendly** for anyone with little or no coding experience. It is even **usable as a Plug-In** in any DAW and can be used to create audio-plugins by exporting a patch as a .VST or .AU plugin via the heavy-compiler integration.

Plug Data makes patching even more comfortable by introducing features such as **automatic object suggestions, signal- and message-flow feedback**, **dynamic patching possibilities** and more.

Comfortability aside – Plug Data offers **two features that are extremely important** for creating our embedded synthesizer with the Daisy Seed. Firstly, it includes the **heavy-compiler**. This will allow us, to **upload (or “flash”) our patch directly from Plug Data onto our microcontroller.** 

<img width="540" alt="Bildschirmfoto 2025-04-22 um 16 13 36" src="https://github.com/user-attachments/assets/e69faecd-58f7-4b33-a3ef-5c2b7f668ed2" />

Secondly, Plug Data includes the **“compiled mode”**, which – when enabled– **marks unsupported objects that cannot be compiled by heavy** and will also e**xclude them from the object suggestions** that pop up while creating a new object. 

<img width="540" alt="Bildschirmfoto 2025-04-22 um 16 16 12" src="https://github.com/user-attachments/assets/5318d019-bc78-45d5-b991-c55a9a1c7d43" />

> We will look at **building a Synthesizer with Plug Data** in [chapter 05]({{site.baseurl}}/chapter-05/05-programming-a-synth)

## → Continue with the next chapter about the Daisy Seed [here]({{site.baseurl}}/chapter-04/04-2-daisy-seed)

