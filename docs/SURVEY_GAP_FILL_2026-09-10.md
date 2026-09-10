# Survey gap-fill (2026-09-10)

Cross-checked Fasano/Wright/Springer/MDPI/Alrawi against tools.jsonl.
See `/workspace/firmware-atlas-work/survey-hunt/CROSSCHECK_IOT_MCU.md`.

## Added this round (conf ≥ 0.85 + public GitHub)
### mcu-firmware-atlas
- AIM
- Hoedur
- SEmu
- AutoMap
- Conware
- Gerbil
- HEAPSTER
- Jetset
- Laelaps
- Perry
- Pretender
- SplITS
- µSBS

### iot-firmware-atlas
- BaseSAFE
- DIANE
- FIRMCORN
- FirmFuzz
- Snipuzz

## Deferred
Low-confidence / paper-only / name-collision items remain in `survey-hunt/gaps_*.jsonl` (Charm, FEMU, Firmalice, MetaEmu arxiv-only, WYCINWYC, PartEmu, …).
Hoedur copied into MCU (was RTOS-only). Fence note: some tools still duplicated across iot+mcu historically — not auto-deduped this round.
