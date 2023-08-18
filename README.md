# EFI Ryzentosh para la Comunidad de ReinierTutoriales
Creare una mini guía para todos los que necesiten instalar macOS en procesadores AMD Ryzen. Tal y como la Dortania pero agregando algunas cosas que para mí son esenciales. Dejando claro cada apartado para mejor comprensión 

## ACPI

## Booter

## DeviceProperties

## Kernel

::: details More in-depth Info

* **FuzzyMatch**: True
  * Used for ignoring checksums with kernelcache, instead opting for the latest cache available. Can help improve boot performance on many machines in 10.6
* **KernelArch**: x86_64
  * Set the kernel's arch type, you can choose between `Auto`, `i386` (32-bit), and `x86_64` (64-bit).
  * If you're booting older OSes which require a 32-bit kernel(ie. 10.4 and 10.5) we recommend to set this to `Auto` and let macOS decide based on your SMBIOS. See below table for supported values:
    * 10.4-10.5 — `x86_64`, `i386` or `i386-user32`
      * `i386-user32` refers 32-bit userspace, so 32-bit CPUs must use this(or CPUs missing SSSE3)
      * `x86_64` will still have a 32-bit kernelspace however will ensure 64-bit userspace in 10.4/5
    * 10.6 — `i386`, `i386-user32`, or `x86_64`
    * 10.7 — `i386` or `x86_64`
    * 10.8 or newer — `x86_64`

## Misc

## NVRAM

## PlatformInfo

## UEFI

## 



## 🌐 Redes Sociales:
[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://www.facebook.com/groups/reiniertutoriales/) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/ReinierTutoriales) [![Telegram](https://img.shields.io/badge/Telegram-%26A5E4.svg?logo=Telegram&logoColor=white)](https://t.me/ReinierTutoriales)


Gracias! :heart:
