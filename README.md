# iot-firmware-atlas

Living map of **IoT / embedded-Linux device firmware** research — acquire, unpack, emulate, analyze — closed-loop taxonomy.

Sibling of [`uefi-firmware-atlas`](https://github.com/vulragrag-star/uefi-firmware-atlas) / [`oss-atlas`](https://github.com/vulragrag-star/oss-atlas).

## Why another list?
We first survey existing awesome/index repos (see `data/seeds/SOURCES.md`), then build a **machine-readable closed-loop atlas** that those lists are not: JSONL schema, use-tags, setting book, smoke notes, explicit domain fences.

## Inclusion / exclusion
- **IN:** Router/camera/NAS/AP embedded Linux firmwares and analysis stacks (binwalk, FACT, EMBA, FirmAE/firmadyne, unpackers).
- **OUT:** Host UEFI/BIOS, Linux kernel syzkaller corpora, bare MCU without Linux userspace, Zephyr-primary RTOS (→ rtos atlas).

## Closed-loop map
See [`docs/MAP.md`](docs/MAP.md), [`docs/TAXONOMY.md`](docs/TAXONOMY.md), [`docs/SETTING.md`](docs/SETTING.md), [`docs/SMOKE.md`](docs/SMOKE.md).

## Status (bootstrap 2026-09-10)
- Seed survey recorded; core tools JSONL: **8** (crawl expansion in flight)
- Papers/vulns/datasets: filling via multi-agent crawl

## Quick start
```bash
python scripts/validate_catalog.py
python scripts/render_catalogs.py
```

## License
Docs: CC BY 4.0. Scripts: MIT. Upstream projects keep their licenses.
