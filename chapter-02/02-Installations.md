---
layout: default
title: 02 Installations
nav_order: 3
---

# 02 Installations

First, we’ll need to make sure you have the right software installed, which we will be needing for our project. We will mainly be needing the following two programs:

-	[Plug Data](https://plugdata.org) will be our main programming environment for creating our instrument. It is based on Pure Data Vanilla, which is a visual programming language for audio applications and more. Plug Data allows for a more comfortable patching than the original Pure Data, which is one of the reasons I chose to use it. Another (and maybe even the more important) reason is that Plug Data includes the heavy-compiler (link) right from the start! We will learn more about the heavy compiler in another chapter (link), but this will be the most important tool to flash our program onto the microcontroller. A third crucial advantage of Plug Data is the “compiled”-mode, which will warn us about uncompilable objects as we program, which makes it very easy not to include those in our patch and therefore ensure that our Instrument will be ready to be flashed onto the Daisy Seed.
![logo](https://github.com/user-attachments/assets/56ea69a6-4de7-4dc6-9ee7-c1a455feab20)



-	[Visual Studio Code](https://code.visualstudio.com) is a coding environment, which allows for a very comfortable coding. We won’t use it too much, as our main programming will take place in Plug Data, but it is an important tool to create our custom JSON-Files (link) which we need so the Daisy Seed will know how to handle Input and Output Signals which we configure in our Plug Data patch. Don’t worry, we will learn more about JSON-Files in this chapter (link).
h![Visual_Studio_Code_1 35_icon svg](https://github.com/user-attachments/assets/b57ca892-dca4-4686-9438-2d0338de484f)



