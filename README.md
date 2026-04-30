<picture>
  <source media="(prefers-color-scheme: dark)" srcset="res/kuro_banner_dark.png">
  <img src="res/kuro_banner.png" alt="KURO banner">
</picture>

# KURO Boot Protocol
[![GitHub license](https://img.shields.io/github/license/TeamSHIRO/kuro-protocol.svg)](LICENSE)

This repository contains the KURO Boot Protocol specification and C headers that can be used to implement the protocol.

You can read the specification here:
[KURO Boot Protocol Specification](docs/protocol.md)

## C headers

C headers are available in the `include` directory of each [`efi`](efi) and [`no_efi`](no_efi) directory.
The headers are split into two directories:
- The [`efi`](efi) contains the kuro headers along with the EFI definitions. Note that the EFI definitions are not fully
  implemented, but it contains all the necessary definitions to access the EFI runtime services and things that are
  related to struct defined in the KURO boot protocol.
- The [`no_efi`](no_efi) contains the kuro headers without the EFI definitions.

Contains the following files in each directory:
- `kuro.h` – Containing the KURO Identifier and common definitions
- `kuro_boot.h` – Containing the KURO Boot Information structure and the related definitions
- `kuro_footer.h` – Containing the KURO Footer structure and the related definitions

## EFI headers

Inside the `efi` directory, there are additional files containing the EFI definitions:
- [`efi.h`](efi/include/efi/efi.h) – Containing the common EFI definitions and the EFI system table definitions
- [`efi_capsule.h`](efi/include/efi/efi_capsule.h) – Containing the EFI definitions for the EFI capsule
- [`efi_conf.h`](efi/include/efi/efi_conf.h) – Containing the EFI definitions for the EFI configuration table and the
  related definitions
- [`efi_misc.h`](efi/include/efi/efi_misc.h) – Containing the EFI definitions for the EFI miscellaneous runtimme
  services
- [`efi_runtime.h`](efi/include/efi/efi_runtime.h) – Containing the EFI definitions for the EFI runtime services
- [`efi_time.h`](efi/include/efi/efi_time.h) – Containing the EFI definitions for the EFI time services
- [`efi_var.h`](efi/include/efi/efi_var.h) – Containing the EFI definitions for the EFI variable services
- [`efi_virtual_mem.h`](efi/include/efi/efi_virtual_mem.h) – Containing the EFI definitions for the EFI virtual memory
  services

## License

The headers are licensed under the Boost Software License, Version 1.0. See the [LICENSE](LICENSE) file or visit
https://www.boost.org/LICENSE_1_0.txt for more information.

The boot protocol documentation is licensed under the
[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).