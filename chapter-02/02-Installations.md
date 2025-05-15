---
layout: default
title: 02 Installations
nav_order: 3
---

# 02 Installations

![PDVS](https://github.com/user-attachments/assets/7d203698-f958-4db0-bb59-8f1e3302fcf9)

First, we’ll need to make sure you have the right software installed, which we will be needing for our project. We will mainly be needing the following two programs:

-	[Plug Data](https://plugdata.org) will be our main programming environment for creating our instrument. It is based on Pure Data Vanilla, which is a visual programming language for audio applications and more. Plug Data allows for a more comfortable patching than the original Pure Data, which is one of the reasons I chose to use it. Another (and maybe even the more important) reason is that Plug Data includes the heavy-compiler (link) right from the start! We will learn more about the heavy compiler in another chapter (link), but this will be the most important tool to flash our program onto the microcontroller. A third crucial advantage of Plug Data is the “compiled”-mode, which will warn us about uncompilable objects as we program, which makes it very easy not to include those in our patch and therefore ensure that our Instrument will be ready to be flashed onto the Daisy Seed.

<img width="540" alt="Bildschirmfoto 2025-05-15 um 12 21 58" src="https://github.com/user-attachments/assets/c4bb71b8-b5a4-474b-9e7a-2bcebef5d095" />
> Simple Example of a Plug Data Patch

-	[Visual Studio Code](https://code.visualstudio.com) is a coding environment, which allows for a very comfortable coding. We won’t use it too much, as our main programming will take place in Plug Data, but it is an important tool to create our custom JSON-Files (link) which we need so the Daisy Seed will know how to handle Input and Output Signals which we configure in our Plug Data patch. Don’t worry, we will learn more about JSON-Files in this chapter (link).

![Bildschirmfoto 2025-05-09 um 14 05 31](https://github.com/user-attachments/assets/0bd3e37a-4817-4de7-842f-65e4a9221b5f)
> Visual Studio Code interface



> Continue with the next chapter about required components [here]({{site.baseurl}}/chapter-03/03-Components)
