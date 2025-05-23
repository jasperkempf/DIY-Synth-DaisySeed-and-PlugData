---
layout: default
title: 04.3 Heavy Compiler Collection (hvcc)
parent: 04 Tools
nav_order: 3
---

# 04.3 Heavy Compiler Collection (hvcc) 

## 📑 hvcc
The heavy compiler collection is a tool to **transform our Pd-Patch into C Code**, so the Daisy Seed can understand it. To explain what hvcc does, I include the following excerpt from the official heavy documentation:

> _“Heavy is a **framework for easily generating audio plugins** for use in interactive sound and music applications such as **games, instruments or installations.**
It aims to **reduce the dependency on low-level programming** from a creative standpoint and **bridge the gap from idea to production-ready implementation.**
Heavy makes use of modern software principles to generate **highly optimised C/C++ code** specifically targeting a wide variety of popular hardware architectures and software frameworks. It can also automatically build plugin binaries for these platforms.”_

We will use heavy through the `compile`-window in Plug Data, aside from its practical use this is all we need to know about it for now. If you want to learn more about heavy, check out their official documentation [here](https://github.com/Wasted-Audio/hvcc).


## ✅ Supported Objects

As heavy interprets our Plug Data Patch and creates a C Code from it, not all objects available in Plug Data can be interpreted by heavy. To know which ones are supported and which are not, it is worth to have a look at the [supported Vanilla objects list](https://github.com/Wasted-Audio/hvcc/blob/develop/docs/09.supported_vanilla_objects.md) and the ❌ [unsupported Vanilla objects list](https://github.com/Wasted-Audio/hvcc/blob/develop/docs/10.unsupported_vanilla_objects.md) in the hvcc documentation. 

Additionally, we can also use all `heavylib`-Objects. Heavylib is a library containing objects, that are specifically created for the use with hvcc. This is really helpful, as some unsupported objects can be substituted with heavylib-objects. We can identify heavylib-objects by their `hv.`-tag, such as in `hv.osc~ sine`.

## 🔐 Compiled Mode

In order to not have to constantly check the list of supported objects to know, if we can use a certain object or not, we can simply turn on the `Compiled Mode` in the **Plug Data dropdown menu** on the top left of the patcher window.

<img width="313" alt="compiled-mode" src="https://github.com/user-attachments/assets/7b2cf893-de0e-40b8-a1de-602555127de5" />

When activated, the **object manager will only show heavy-supported objects.** While we can still manually add other objects to our patch, **unsupported ones are marked by a orange outline.** By activating `compiled mode`, **we can patch freely with the available objects** and **don't need to worry** about compatibility with hvcc.

We will look at the detailed steps of compiling and flashing a patch with heavy in <a href="{{ site.baseurl }}/chapter-07/07-flashing-a-patch">chapter 07 →</a>

## ⚠️ Known limitations
Read more about Tips and Tricks using the heavy compiler as well as known limitations [here](https://github.com/Wasted-Audio/hvcc/blob/develop/docs/02.getting_started.md)


## → Continue with the next chapter about JSON-Files [here]({{site.baseurl}}/chapter-04/04-4-json-file)
