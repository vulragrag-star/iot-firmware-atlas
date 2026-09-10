# TAXONOMY — iot-firmware-atlas

Sibling of [uefi-firmware-atlas](https://github.com/vulragrag-star/uefi-firmware-atlas). Same closed-loop stages and use-tags.

## Inclusion
Router/camera/NAS/AP embedded Linux firmwares and analysis stacks (binwalk, FACT, EMBA, FirmAE/firmadyne, unpackers).

## Exclusion
Host UEFI/BIOS, Linux kernel syzkaller corpora, bare MCU without Linux userspace, Zephyr-primary RTOS (→ rtos atlas).

## Stages
spec | acquire | parse | static_re | emulate_fuzz | runtime_assess | offense_poc | defend_harden | vuln_intel | dataset | paper_map | lab_teaching

## Series
See [uefi docs/SERIES.md](https://github.com/vulragrag-star/uefi-firmware-atlas/blob/main/docs/SERIES.md).
