# musicality_db

## Merge dataset

The `merge` dataset combines tracks from `ballroom`, `rwc_classical`, `rwc_genre`, `rwc_jazz`, `rwc_popular`, and `jtd` into a single set of splits per task. Splits live under `splits/merge` (task: `beat`) and `splits/beat_phase-merge-binary` (task: `beat_phase_binary`).

`beat` (`splits/merge`) is one entry per track. `beat_phase_binary` (`splits/beat_phase-merge-binary`) is one entry per beat-phase segment, so its counts don't match `beat` 1:1 — segments are chunked from tracks.

| version | beat train | beat val | beat_phase_binary train | beat_phase_binary val |
|---------|-----------:|---------:|-------------------------:|-----------------------:|
| v8.1.0 | **2124** | **335** | **1854** | **277** |
| v8.0.0 | **2056** | **318** | **1792** | **262** |
| v7.0.0 | **2001** | **304** | **1738** | **249** |
| v6.0.0  | **809** | **200** | **629** | **152** |

### Constituent datasets

| Source        | beat train | beat val | beat_phase_binary train | beat_phase_binary val |
|---------------|-----------:|---------:|-------------------------:|-----------------------:|
| ballroom | 559 | 139 | 419 | 104 |
| gtzan | 124 | 31 | 117 | 28 |
| jtd | 1190 | 103 | 1107 | 96 |
| rwc_classical | 49 | 12 | 32 | 7 |
| rwc_genre | 82 | 20 | 68 | 16 |
| rwc_jazz | 40 | 10 | 31 | 7 |
| rwc_popular | 80 | 20 | 80 | 19 |
