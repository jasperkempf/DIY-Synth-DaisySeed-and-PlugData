---
layout: default
title: 05.2 Filters
parent: 05 Programming a Synthesizer
nav_order: 2
---

# 05.2 Filters
### 📥 Download all example Patches <a href="{{ site.baseurl }}/assets/diy-synth-example-files.zip" download>here</a> !
> 📖 The example patch for this chapter is `_Pd03-Filter-Examples_`.

## 🧪 Filters
Now that we've learned how to program heavy-compatible oscillators, we will add a filter to our synthesizer. Here we can also use objects from the heavylib-Library. It comes with the `hv.filter~ `-object, **which can be configured for one of six different filtercurves** – allpass, lowpass, highpass, bandpass1, bandpass2 and notch. 

> The example patch _pd03-Filter-Examples.pd_ shows how i implemented **four of those filter types**. I have used the same custom `counter`-mechanism from the previous chapter to **select different filter types** with a simple `bang`. 

<img width="1080" alt="Bildschirmfoto 2025-04-29 um 10 51 25" src="https://github.com/user-attachments/assets/a3af22cc-d35c-4c29-bf36-5c0147c6c7fd" />

Opening the subpatch _pd Filters_ gives us insight into the mechanism, which lets us choose the **different filter types**. As the `select~` is not compilable, i used the same custom counter-operation as with our oscillators. 

As it feeds the numbers 1 to 4 into the `route 1 2 3 4`-object, it will **activate only the selected filter type**, that corresponds to the selected number, while deactivating all others. As previously achieved, activating and deactivating is achieved **by a simple signal multiplication** with either `0.5` or ` 0 `.

<img width="1080" alt="05-02-pd03-FiltersSubpatch" src="https://github.com/user-attachments/assets/1240613e-b047-4699-a10f-561f26be4ef0" />

> ✅ We can now **choose different oscillators and different filter types** via a bang signal. Let's have a look at implementing modulation into our synth, to expand its' sonic capabilities further! 

## → Continue with the next chapter about modulation [here]({{site.baseurl}}/chapter-05/05-3-Modulation)

