---
layout: default
title: 02 Installations
nav_order: 3
---

# 02 Installations

![PDVS](https://github.com/user-attachments/assets/7d203698-f958-4db0-bb59-8f1e3302fcf9)

First, we’ll need to make sure you have the right software installed, which we will be needing for our project. We will mainly be needing the following two programs:

-	[Plug Data](https://plugdata.org) will be our **main programming environment for creating our instrument**. It is based on Pure Data Vanilla, which is a visual programming language for audio applications and more. Plug Data allows for a more comfortable patching than the original Pure Data, which is one of the reasons I chose to use it. Another (and maybe even the more important) reason is that P**lug Data includes the heavy-compiler**. We will learn more about the heavy compiler in [another chapter]({{site.baseurl}}/chapter-04/04-3-hvcc), but this will be the most **important tool to flash our program onto the microcontroller.** 

-	[Visual Studio Code](https://code.visualstudio.com) is a **coding environment,** which allows for a very comfortable coding. We won’t use it too much, as our **main programming will take place in Plug Data**, but it is an important tool to create our **custom JSON-Files** which we need so the Daisy Seed will know **how to handle Input and Output Signals** configured in our Plug Data patch. Don’t worry, we will learn more about JSON-Files in [this chapter]({{site.baseurl}}/chapter-04/04-4-json-file).


**This graphic shows how the Plug Data Patch and the JSON-File are connected and need to be flashed together:**

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 15 56 51" src="https://github.com/user-attachments/assets/eec669fa-54f1-40db-a1ce-61afb33fa538" />



> Continue with the next chapter about required components [here]({{site.baseurl}}/chapter-03/03-Components)
