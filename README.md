## 🌐 Redes 👇
[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://www.facebook.com/groups/reiniertutoriales/) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/ReinierTutoriales) [![Telegram](https://img.shields.io/badge/Telegram-%26A5E4.svg?logo=Telegram&logoColor=white)](https://t.me/ReinierTutoriales) [![Cómprame un :tea:](https://github.com/ReinierTutoriales/ReinierTutoriales/blob/main/imagenes/paypal.svg)](https://www.paypal.com/paypalme/ReinierTutoriales)


# EFI Ryzentosh para la Comunidad de ReinierTutoriales
Creare una mini guía para todos los que necesiten instalar macOS en procesadores AMD Ryzen. Tal y como la Dortania pero agregando algunas cosas que para mí son esenciales. Dejando claro cada apartado para mejor comprensión.

# Consideraciones a tener en cuenta.
- [x] Esta EFI tiene SSDT genéricos de Dortania para mejorar la compatibilidad con el máximo de equipos.
- [x] Si vas a instalar para gráficos integrados AMD  en APU tienes que remover [WhateverGreen.kext](https://dortania.github.io/builds/?product=WhateverGreen&viewall=true) y incorporar [NootedRed.kext](https://github.com/NootInc/NootedRed).

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
- [x] Desactivar en la BIOS.
     - Fast Boot
     - Secure Boot
     - Serial/COM Port
     - Parallel Port
     - Compatibility Support Module CSM debe estar desactivado en la mayoría de los casos, los errores de GPU gIO son comunes cuando esta opción está habilitada.
     - IOMMU





