# Third-party notices

This repository and its release files contain work by OpenSourceSDRLab together with third-party software. The Apache License 2.0 in [LICENSE](LICENSE) applies **only** to the files created by OpenSourceSDRLab:

- `docs/`, `hardware/`, `images/`, `README.md`
- in each `vivado/<design>/` folder:
  - `FMC_AD9371_PL/src/axi_lite_drv.v`
  - `FMC_AD9371_PL/src/jesd204_transport_layer.v`
  - `FMC_AD9371_PL/src/jesd204b_adc_dac_top.v`
  - `FMC_AD9371_PL/JESD204B_TX_RX.srcs/constrs_1/new/system.xdc`
  - `FMC_AD9371_PS/src/headless.c`
  - `FMC_AD9371_PS/ad9371/`: `change_rfpll.c`, `change_rfpll.h`, `rf_config.c`, `rf_config.h`, `README.md`

All other files keep their original copyright notices and licences, which have not been changed:

| Component | Files | Owner | Licence |
|---|---|---|---|
| AD9371 (Mykonos) API, version 1.5.1 | `FMC_AD9371_PS/mykonos/` | Analog Devices, Inc. | AD9371 API licence (*API Source Code Software License Agreement, 20130524-CISC-CTSLA*), full text in `FMC_AD9371_PS/LICENSE.txt` |
| AD9528 driver and AD9371 platform helpers | `FMC_AD9371_PS/ad9528/`, `FMC_AD9371_PS/drivers/common.c`, `common.h` | Analog Devices, Inc. | AD9371 API licence, see `FMC_AD9371_PS/LICENSE.txt` |
| AD9371 radio profile and clock set-up (modified) | `FMC_AD9371_PS/ad9371/myk.c`, `myk.h`, `FMC_AD9371_PS/ad9528/myk_ad9528init.c` | Analog Devices, Inc. | AD9371 API licence, see `FMC_AD9371_PS/LICENSE.txt`. Generated with the Analog Devices transceiver evaluation software and then adapted for this board (JESD204B framer, gain-control and SPI chip-select settings) |
| Profile files exported from the Analog Devices transceiver evaluation software | `FMC_AD9371_PS/AD9371_Trans_Create/` | Analog Devices, Inc. | AD9371 API licence, see `FMC_AD9371_PS/LICENSE.txt` |
| ADI no-OS platform drivers and JESD204 drivers | `FMC_AD9371_PS/drivers/no_os_*`, `xilinx_gpio.*`, `xilinx_spi.*`, `FMC_AD9371_PS/ad9371/jesd_core.c`, `jesd_core.h`, `jesd_phy.c`, `jesd_phy.h`, `FMC_AD9371_PS/src/parameters.h` | Analog Devices, Inc. | as stated in each file header (`jesd_phy.h` has no notice of its own and is distributed with `jesd_phy.c` under its terms) |
| ADI HDL modules | `FMC_AD9371_PL/src/ad_iobuf.v`, `up_axi.v` | Analog Devices, Inc. | as stated in each file header |
| Mykonos ARM firmware 5.1.1 (object code inside the prebuilt application `.elf` and `BOOT.bin` in Releases) | Releases only | Analog Devices, Inc. | Firmware Software License Agreement (20180301-AD937X-CTSLA) |
| Xilinx/AMD IP cores, block design, linker script and generated files | `FMC_AD9371_PL/` (`.xpr`, `.xci`, `.bd` and generated files), `FMC_AD9371_PS/src/lscript.ld`, `Xilinx.spec`, the `.xsa` files, and the Xilinx parts of the prebuilt `.bit`, `.xsa`, `fsbl.elf` and `BOOT.bin` in Releases | Xilinx, Inc. / AMD | Xilinx/AMD licence terms |

Some Analog Devices files were adapted for this board before they were published here (most visibly the radio profile in `myk.c`). As the AD9371 API licence requires, they are marked as modified in the table above; their copyright notices are unchanged. The Analog Devices notice that was missing from `myk_ad9528init.c` has been put back (copied from the original Analog Devices file in `AD9371_Trans_Create/122.8_ad9528init.c`).

Files and software that are **not** included and must be obtained from Analog Devices:

- the Mykonos ARM firmware header `Mykonos_M3.h` (version 5.1.1), needed to build the application from source. Its licence only allows distribution as object code inside a product. Download instructions and checksum: `vivado/<design>/FMC_AD9371_PS/ad9371/README.md`;
- the AD9371 Transceiver Evaluation Software: <https://www.analog.com/en/products/ad9371.html>.

"Analog Devices", "AD9371", "AD9528", "Mykonos", "Xilinx", "Zynq", "Vivado" and "Vitis" are trademarks of their respective owners. They are used here only to describe compatibility and do not imply endorsement.
