# hackintosh-asus-x550vx
A raw guide to remember

## What the F?
This is Apple's the best thing since sliced bread called MacOS that installed into non-Apple products.
In this case I use Asus X550VX and installed `MacOS Catalina 10.15.2`

Before we start, something important that everyone have to know before do this job is knowing the hardware specs, and here is my laptop's spesification:
* Processor : **Intel i7-6700**
* Wifi Adapter : **Atheros AR9285**
* RAM : 8 GB
* SSD : Samsung EVO 120GB
* Audio : Unchecked, but it used `ALC255` on post-installation.

## Jump to Hacki
### Back Up
It always come first when you do OS Installation, just in case you need your data so bad!

### Create USB Bootable
Put it in your mind that it needs more than 8GBs of free space USB, the 16GB are recommended!

Two ways that i've ever tried for installation is using *multibeast* and *balena etcher*. But when I use windows, I'll using *Transmac*.
The image that i used is coming from *Olarila*, a real vanilla OS as it said. Except you use *multibeast* you have to download it from the store!

### Instalation
I can't show you the step, but it's ez af. But disable boot security first!
* Boot into flashdrive
* Go to *configuration* or type `o`
* Change `config` into `config2` for laptop, because `config` is only for PC
* Boot Installation
* Clean up the disk first
* Install Catalina

### Post-Instalation
* Install Clover (It's in the **FILES** directory)
* Copy **Clover Configurator** into `/Application`
* Mount `/EFI` from Disk (and Flashdrive).
* Replace everything inside `/EFI` on Disk with `/EFI` on Flashdrive
* Reboot and unplug the USB, if it could boot from clover, it works.
* Mount `/EFI` from Disk and Browse
* Jump into `/EFI/EFI/CLOVER/`
* In `Kext` directory, you'll see **Other** directory, replace is with **Other** from this repo
* Replace `config.plist` with repo's `config.plist`
* And in `/EFI/EFI/CLOVER/ACPI` save `DSDT.aml` into `patched` directory
