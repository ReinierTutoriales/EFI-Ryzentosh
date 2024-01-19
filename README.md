<div id="header" align="center">
  <img src="https://github.com/ReinierTutoriales/ReinierTutoriales/blob/main/imagenes/Logo%20RT.png" width="150"/>

## 🌐 Redes 👇
[![](https://img.shields.io/badge/YouTube-informational?style=for-the-badge&logo=telegram&logoColor=white&color=FF0000)](https://youtube.com/c/ReinierTutoriales)
[![](https://img.shields.io/badge/PayPal-informational?style=for-the-badge&logo=paypal&logoColor=white&color=003087)](https://www.paypal.com/paypalme/ReinierTutoriales)
[![](https://img.shields.io/badge/-Telegram-informational?style=for-the-badge&logo=telegram&logoColor=white&color=0088cc)](https://t.me/ReinierTutoriales)
[![](https://img.shields.io/badge/-Twitter-informational?style=for-the-badge&logo=twitter&logoColor=white&color=00aced)](https://twitter.com/ReinierTutorial)
[![](https://img.shields.io/badge/-Facebook-informational?style=for-the-badge&logo=facebook&logoColor=white&color=3b5998)](https://www.facebook.com/groups/reiniertutoriales/)
[![](https://img.shields.io/badge/-Instagram-informational?style=for-the-badge&logo=instagram&logoColor=white&color=C13584)](https://www.instagram.com/reiniertutoriales/)

<hr>

 Ryzentosh AMD
==========================================

[![Static Badge](https://img.shields.io/badge/macOS-Ventura-blue)](https://www.reiniertutoriales.com/topic/96-iso-booteable-de-macos-ventura-1351/)
[![Static Badge](https://img.shields.io/badge/OpenCore-0.9.5-green)](https://github.com/dortania/build-repo/releases/download/OpenCorePkg-2bbda9d/OpenCore-0.9.5-RELEASE.zip)
[![GitHub issues](https://img.shields.io/github/issues/ReinierTutoriales/EFI-Ryzentosh)](https://github.com/ReinierTutoriales/EFI-Ryzentosh/issues)



</div>



# EFI Ryzentosh para la Comunidad de ReinierTutoriales
Creare una mini guía para todos los que necesiten instalar macOS en procesadores AMD Ryzen. Tal y como la Dortania pero agregando algunas cosas que para mí son esenciales. Dejando claro cada apartado para mejor comprensión.


# Consideraciones a tener en cuenta.
- [x] Esta EFI tiene SSDT genéricos de Dortania para mejorar la compatibilidad con el máximo de equipos.
- [x] Si vas a instalar para gráficos integrados AMD  en APU tienes que remover [WhateverGreen.kext](https://dortania.github.io/builds/?product=WhateverGreen&viewall=true) y incorporar [NootedRed.kext](https://github.com/ChefKissInc/NootedRed).
- [x] Esta EFI carece de serial por lo que deberá ser generado con [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS), ya que cada equipo necesita uno y duplicarlo puede traer graves consecuencias.

### Estructura EFI
## ACPI
- SSDT-EC-USBX.aml
## Drivers
- HfsPlus.efi
- OpenCanopy.efi
- OpenRuntime.efi
- ResetNvramEntry.efi
- ToggleSipEntry.efi
## Kexts
- AppleALC.kext
- AppleMCEReporterDisabler.kext
- IntelMausi.kext
- Lilu.kext
- NVMeFix.kext
- RealtekRTL8111.kext
- RestrictEvents.kext
- VirtualSMC.kext
- WhateverGreen.kext
## Tools
- OpenShell.efi
- ResetSystem.efi

# Configuración EFI por Apartados. 
## ACPI
| SSDTs Requeridos| Description |
| :--- | :--- |
| **[SSDT-EC-USBX](https://dortania.github.io/Getting-Started-With-ACPI/)** | Repara tanto el controlador integrado como la alimentación USB. |
| **[SSDT-CPUR](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-CPUR.aml)** | Corrección para CPU con placas base B550 y A520, `usar solo si tienes B550 o A520`.|

- [x] Esta EFI no tiene `SSDT-CPUR.aml` pero puede descargarlo y agregarlo a su `config.plist` si tiene Motherboard B550 y A520.

## Booter

## DeviceProperties

## Kernel

## Misc

## NVRAM

## PlatformInfo

## UEFI

## Configuración en la BIOS
- [x] Deshabilitar en la BIOS.
     - Fast Boot
     - Secure Boot
     - Serial/COM Port
     - Parallel Port
     - Compatibility Support Module CSM debe estar desactivado en la mayoría de los casos, los errores de GPU gIO son comunes cuando esta opción está habilitada.
     - IOMMU
 
 - [x] Habilitar en la BIOS.
      - Above 4G Decoding
      - Resize Apple GpuBars Actívalo en graficas de serie RX 6000 .
      - EHCI/XHCI Hand-off
      - OS type: Windows 8.1/10 UEFI Mode
      - SATA Mode: AHCI





