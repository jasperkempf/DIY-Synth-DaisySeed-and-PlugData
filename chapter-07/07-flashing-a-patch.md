## 07 Compiling and flashing a patch

Using the hvcc integration, we can flash a patch directly from Plug Data onto our Daisy Seed Microcontroller. To do that, we first need to to set the Daisy Seed to Bootloader-Mode, which will allow flashing a new patch. This is done via the onboard-buttons of the Daisy as follows:

1. Press and hold the `Boot`-button
2. Press and hold the `Reset`-button
3. Let go of the `Reset`-button
4. Let go of the `Boot`-button

Having the Daisy connected to our computer via the USB-cable, **we can now flash our patch via the `compile`-section,** which can be found via the dropdown-menu in the top left corner. Here we select `Electro-Smith Daisy`, as well as the patch to be flashed and our JSON-File. As export-Type we choose `Flash`. 

**Depending on your project, you need to specify the size in the `Patch-Size`-category.** Depending on the size, the Patch will be flashed to different memories of the Daisy. Choosing `SMALL` will flash the patch to the **internal flash memory,** which has 128kB of storage. **If your project exceeds this size, you should select other options** such as `BIG` - which will flash to SRAM (480kB) - or `BIG + SDRAM`, which will make **additional use of the SDRAM-memory.** When exporting, the **compile window gives us insights of the used memory-region** (you might have to scroll up a bit) as well as the amount of used percentage per region. Note that the amount of available SDRAM-Storage can be either 8MB or 64MB, depending on your version of the Daisy Seed.

<img width="651" alt="memory regions" src="https://github.com/user-attachments/assets/b5e2697c-44d0-47a0-bb09-2064ac5cab96" />

When selecting another option than `SMALL`, **the compiler will load the Bootloader into the flash-memory.** This is a program that will **boot our flashed patch from other memory-regions,** such as the SRAM.
