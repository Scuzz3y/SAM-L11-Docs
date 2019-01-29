http://ww1.microchip.com/downloads/en/DeviceDoc/SAM-L10L11%20Family-DataSheet%20-%20DS60001513B.pdf

13.2.2.1: Flash
Describes the regions of flash for the SAM L11.
Table of Memory region, base address of region, and size of the region.

| Memory region                         |              Base address              |                                                                Size |
| :------------------------------------ | :------------------------------------: | ------------------------------------------------------------------: |
| Flash Boot area                       |               0x00000000               |                                                 BOOTPROT * 256Bytes |
| Flash Secure Boot                     |               0x00000000               |                                          BS*256Bytes - BNSC*32Bytes |
| Flash Non-Secure Callable Boot        |    Contiguous to Flash Secure Boot     |                                                      BNSC * 32Bytes |
| Flash Non-Secure Boot (1)             |             BS * 256Bytes              |       Flash Boot remaining size (BOOTPROT * 256Bytes - BS*256Bytes) |
| Flash Appliation area                 |          BOOTPROT * 256Bytes           |                  Flash size - BOOTPROT * 256Bytes (Flash Boot area) |
| Flash Secure Application              |          BOOTPROT * 256Bytes           |                                            AS*256Bytes-ANSC*32Bytes |
| Flash Non-Secure Callable Application | Contiguous to Flash Secure APPLICATION |                                                      ANSC * 32Bytes |
| Flash Non-Secure Application          |        (BOOTPROT+AS) * 256Bytes        | Flash remaining size (Flash size - BOOTPROT*256Bytes - AS*256Bytes) |
| Secure Data Flash                     |               0x00400000               |                                                       DS * 256Bytes |
| Non-Secure Data Flash                 |    Contiguous to Secure Data Flash     |                                        2KB - Secure Data Flash size |
| Secure SRAM                           |               0x20000000               |                                                       RS * 128Bytes |
| Non-Secure SRAM                       |       Contiguous to Secure SRAM        |                                        SRAM size - Secure SRAM size |