---
layout: default
title: 02 Installations
nav_order: 3
---

# 02 Installations

![PDVS](https://github.com/user-attachments/assets/7d203698-f958-4db0-bb59-8f1e3302fcf9)

First, we’ll need to make sure you have the right software installed, which we will be needing for our project. We will mainly be needing the following two programs:

-	[Plug Data](https://plugdata.org) will serve as our primary programming environment for building the instrument.
It is based on Pure Data Vanilla, a visual programming language designed for audio and multimedia applications. Plug Data provides a more user-friendly patching experience than the original Pure Data, which is one of the main reasons I chose it.

Another — perhaps even more important — reason is that Plug Data includes the Heavy Compiler. We’ll explore this tool in more detail in [another chapter]({{site.baseurl}}/chapter-04/04-3-hvcc), but for now, just know that it’s essential for compiling and flashing our program onto the microcontroller.

-	[Visual Studio Code](https://code.visualstudio.com) is a **coding environment,** which allows for a very comfortable coding. We won’t use it too much, as our **main programming will take place in Plug Data**, but it is an important tool to create our **custom JSON-Files** which we need so the Daisy Seed will know **how to handle Input and Output Signals** configured in our Plug Data patch. Don’t worry, we will learn more about JSON-Files in [this chapter]({{site.baseurl}}/chapter-04/04-4-json-file).


**This graphic shows how the Plug Data Patch and the JSON-File are connected and need to be flashed together:**

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 15 56 51" src="https://github.com/user-attachments/assets/eec669fa-54f1-40db-a1ce-61afb33fa538" />



> Continue with the next chapter about required components [here]({{site.baseurl}}/chapter-03/03-Components)
