# Mykonos ARM firmware header (not included)

The bare-metal application loads the AD9371 ARM processor firmware from one header file supplied by Analog Devices:

| File | Contents |
|---|---|
| `Mykonos_M3.h` | AD9371 (Mykonos) ARM firmware, version 5.1.1, as the C array `firmware_Mykonos_M3_bin[]` |

It is released by Analog Devices under the *Firmware Software License Agreement (20180301-AD937X-CTSLA)*, which allows it to be distributed only as object code inside a product. It is therefore not stored in this repository. Download it from Analog Devices and place it in this folder (`FMC_AD9371_PS/ad9371/`, next to `rf_config.c`, which includes it) before building.

**Use the same version this design was tested with** (Mykonos API 1.5.1.3565, ARM firmware 5.1.1). It is on the `2018_R1` release branch of Analog Devices' no-OS repository:

- <https://github.com/analogdevicesinc/no-OS/blob/2018_R1/ad9371/sw/Mykonos_M3.h>

```sh
curl -LO https://raw.githubusercontent.com/analogdevicesinc/no-OS/2018_R1/ad9371/sw/Mykonos_M3.h
```

Check the download (it must match exactly):

```
a9056953f65975b4e0d58e977b7fb8b86775e0ad3d90b497e1d8a9ad38a5b406  Mykonos_M3.h
```

Later no-OS branches (`2018_R2` and newer) carry a newer firmware build that has not been tested with this design.

The prebuilt application `.elf` files and `BOOT.bin` in the Releases already contain this firmware in object-code form.
