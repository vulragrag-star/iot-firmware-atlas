# IoT firmware tools crawl summary

Generated: 2026-09-10 16:14 CST (Asia/Shanghai)

## Totals
- In-scope catalog entries: **149** (success criterion ≥60)
- Papers: **25** (criterion ≥20)
- Vulns: **14** (criterion ≥10)
- Datasets: **9** (criterion ≥5)
- Stars/last_push/license/language: live `gh api` metadata
- Seeds: fkie-cad/awesome-embedded-and-iot-security, hexsecs/awesome-embedded-security, H4lo/awesome-IoT-security-article, f1tao/awesome-iot-security-resource, kayranfatih/awesome-iot-and-hardware-security
- Expansion queries: binwalk, firmadyne, FirmAE, EMBA, FACT firmware, firmwalker, sasquatch, jefferson, ubi_reader, firmware analysis toolkit + topic expansions (unblob, ofrak, Karonte, SaTC, FirmAFL, IoTGoat, DVRF, emux, …)
- Method: gh API / gh search / WebFetch only — **no repo clones**

## Counts by closed_loop_stage
| stage | count |
|-------|------:|
| spec | 8 |
| acquire | 3 |
| parse | 34 |
| static_re | 24 |
| emulate_fuzz | 26 |
| runtime_assess | 8 |
| offense_poc | 7 |
| defend_harden | 2 |
| vuln_intel | 6 |
| dataset | 1 |
| paper_map | 12 |
| lab_teaching | 18 |
| **total** | **149** |

## Top 15 must-have tools

- **binwalk** (14328★) — `parse` — Firmware signature scanner and extractor (binwalk). — https://github.com/ReFirmLabs/binwalk
- **emba** (3653★) — `runtime_assess` — EMBA — automated Linux firmware security analyzer. — https://github.com/e-m-b-a/emba
- **FACT_core** (1465★) — `runtime_assess` — FACT — Firmware Analysis and Comparison Tool. — https://github.com/fkie-cad/FACT_core
- **unblob** (2552★) — `parse` — Extraction engine for many container/filesystem formats. — https://github.com/onekey-sec/unblob
- **firmadyne** (2105★) — `emulate_fuzz` — Emulate and dynamically analyze Linux-based firmware. — https://github.com/firmadyne/firmadyne
- **FirmAE** (927★) — `emulate_fuzz` — FirmAE — large-scale IoT firmware emulation improvements. — https://github.com/pr0v3rbs/FirmAE
- **firmware-analysis-toolkit** (1595★) — `lab_teaching` — FAT — meta toolkit wiring IoT FW analysis tools. — https://github.com/attify/firmware-analysis-toolkit
- **ofrak** (2070★) — `parse` — OFRAK — unpack, analyze, modify, repack binaries/firmware. — https://github.com/redballoonsecurity/ofrak
- **IoTGoat** (931★) — `lab_teaching` — IoTGoat — deliberately insecure OpenWrt-based firmware. — https://github.com/OWASP/IoTGoat
- **routersploit** (13241★) — `offense_poc` — Exploitation Framework for Embedded Devices (research/lab). — https://github.com/threat9/routersploit
- **cwe_checker** (1355★) — `static_re` — Find CWE-style vulnerable patterns in binaries (ELF ARM/MIPS/x86). — https://github.com/fkie-cad/cwe_checker
- **FirmAFL** (463★) — `emulate_fuzz` — FIRM-AFL — high-throughput greybox fuzzer for IoT firmware. — https://github.com/zyw-200/FirmAFL
- **emux** (872★) — `emulate_fuzz` — EMUX (formerly ARMX) firmware emulation framework. — https://github.com/therealsaumil/emux
- **karonte** (430★) — `static_re` — Karonte — multi-binary taint analysis for IoT firmware. — https://github.com/ucsb-seclab/karonte
- **openwrt** (28347★) — `spec` — OpenWrt — Linux distro for embedded devices/routers. — https://github.com/openwrt/openwrt

## Exclusion notes (tempting misses / domain fences)
- chipsec / UEFITool / edk2 / fwupd — host UEFI/platform → **uefi-firmware-atlas**
- syzkaller / kernel-hardening-checker / linux-exploit-suggester — Linux kernel → **linux-kernel-atlas**
- Zephyr / FreeRTOS / RT-Thread / MCUBoot / ESP-IDF / OpenOCD / ChipWhisperer — RTOS/MCU → **rtos-** / **mcu-firmware-atlas**
- craigz28/firmwalker — original GitHub repo unavailable; catalog uses surviving forks (`misterch0c/firmwalker`, `zhibx/firmwalker_pro`, …)
- Killerbee / Proxmark / Bettercap / SDR stacks — RF/protocol HW toolkits, not FW image unpack/emulate core (listed only if fringe HW-acquire)
- SpiderFoot / phoneinfoga / recon-ng — OSINT, not firmware analysis
- ScoutSuite / Vulhub generic — cloud/generic vuln envs, not IoT FW dumps
- HAL (emsec/hal) gate-level netlist RE — IC hardware, not device firmware images
- PreOS-Security/awesome-firmware-security — explicitly less IoT-OS; cross-link only / fringe paper_map

## Fringe (included with notes)
- coolsnowwolf/lede, immortalwrt — regional OpenWrt forks
- FirmWire — cellular baseband (IoT-adjacent)
- HALucinator / Fuzzware — MCU-leaning rehosting/fuzz (kept fringe for survey completeness)
- PRET — printers (networked device adjacent)
- CyberChef / pwntools / Ghidra / radare2 / angr — general RE stack heavily used in IoT FW labs
- flashrom / tuya-cloudcutter — physical/Wi-Fi acquire paths

## Gaps
- **Original firmwalker** upstream gone; forks diverge — need a maintained canonical fork note
- **Large public redistributable FW dump corpora** rare (Firmadyne-scale images not legally mirrored); mostly BYO vendor downloads
- **RTOS/MCU depth** intentionally deferred to sibling atlases (success text allowed ≥40 there if sparse — IoT itself is dense)
- **Vendor-specific unpackers** incomplete (many OEM cameras/routers still undocumented)
- **Baseband / automotive / Zigbee** only lightly covered (fringe)
- **Live smoke** of lab-usable subset (binwalk/unblob/EMBA Docker/IoTGoat) not executed this pass
- **Paper→artifact links** incomplete for older works (Firmalice, Costin scrapers)

## Scope reminders
- **IN**: Router/camera/NAS/AP embedded Linux firmwares — binwalk, FACT, EMBA, Firmadyne/FirmAE, firmwalker, unpackers, FAT, OpenWrt-class trees, IoTGoat/DVRF
- **OUT**: Host UEFI/BIOS, Linux syzkaller, bare MCU blink, Zephyr-as-primary

## Smoke notes
- Crawl is metadata + curated classification; in-VM smoke of lab-usable subset not executed this pass.
- Practical starters: binwalk/unblob → sasquatch/jefferson/ubi_reader → firmwalker/trommel → EMBA or FACT → FirmAE/emux for dynamic → IoTGoat/DVRF for teaching.
