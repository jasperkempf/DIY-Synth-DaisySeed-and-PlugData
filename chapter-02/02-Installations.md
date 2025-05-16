---
layout: default
title: 02 Installations
nav_order: 3
---

# 02 Installations

![PDVS](https://github.com/user-attachments/assets/7d203698-f958-4db0-bb59-8f1e3302fcf9)

First, we need to make sure the required software is installed. The two main programs we will rely on are:

-	[Plug Data](https://plugdata.org) will serve as our **primary programming environment for building the instrument.**
It is based on **Pure Data Vanilla**, a visual programming language designed for audio and multimedia applications. Plug Data provides a more **user-friendly patching experience** than the original Pure Data, which is one of the reasons I chose it. Another — perhaps even more important — reason is that **Plug Data includes the heavy Compiler**. We’ll explore this tool in more detail in [another chapter]({{site.baseurl}}/chapter-04/04-3-hvcc), but for now, just know that **it’s essential for compiling and flashing our program** onto the microcontroller.

- [Visual Studio Code](https://code.visualstudio.com) is a **powerful and user-friendly code editor.** While we won’t use it extensively — since most of our programming will happen in Plug Data — it plays an important role in **creating custom JSON files**. These JSON files are necessary for telling the Daisy Seed **how to handle the input and output signals** defined in our Plug Data patch. Don’t worry — we’ll cover everything you need to know about JSON files later in [this chapter]({{site.baseurl}}/chapter-04/04-4-json-file).

**The graphic below illustrates how the Plug Data patch and the JSON file are connected, and why both need to be flashed together onto the device:**

<img width="1080" alt="Bildschirmfoto 2025-05-15 um 15 56 51" src="https://github.com/user-attachments/assets/eec669fa-54f1-40db-a1ce-61afb33fa538" />



> Continue with the next chapter about required components [here]({{site.baseurl}}/chapter-03/03-Components)
