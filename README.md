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

## Status (crawl merge 2026-09-10)
- Tools: **149** (fringe flagged: **69**)
- Papers / vulns / datasets: **25** / **14** / **9**
- Seeds first: fkie-cad awesome-embedded-and-iot · hexsecs · … — `data/seeds/SOURCES.md` · `docs/CRAWL_SUMMARY.md`

### Tool counts by stage

| Stage | n |
|---|---|
| acquire | 3 |
| dataset | 1 |
| defend_harden | 2 |
| emulate_fuzz | 26 |
| lab_teaching | 18 |
| offense_poc | 7 |
| paper_map | 12 |
| parse | 34 |
| runtime_assess | 8 |
| spec | 8 |
| static_re | 24 |
| vuln_intel | 6 |
| **total** | **149** |


## Quick start
```bash
python scripts/validate_catalog.py
python scripts/render_catalogs.py
```

## License
Docs: CC BY 4.0. Scripts: MIT. Upstream projects keep their licenses.
