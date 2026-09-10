# Method — iot-firmware-atlas

1. Harvest seed awesome/index lists in `data/seeds/`.
2. Expand via GitHub search/topics + paper artifacts.
3. Normalize to `data/*.jsonl` per `data/schema.json`.
4. Gate with inclusion/exclusion in `docs/TAXONOMY.md`; rejects → `data/rejected.jsonl`.
5. Enrich stars via gh API (never invent).
6. Render `catalogs/` ; smoke `lab-usable` rows on Linux VM when possible.
