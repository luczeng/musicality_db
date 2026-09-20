# musicality_db

## Merge dataset

The `merge` dataset combines tracks from `ballroom`, `rwc_classical`, `rwc_genre`, `rwc_jazz`, `rwc_popular`, and `jtd` into a single set of splits per task. Splits live under `splits/merge` (task: `beat`) and `splits/merge-binary` (task: `binary`).

Both tables are one entry per track. `binary` (`splits/merge-binary`) only covers the tracks annotated for the binary task, so its counts don't match `beat` 1:1.

| version | beat train | beat val | binary train | binary val |
|---------|-----------:|---------:|-------------:|-----------:|
| v9.1.0 | **810** | **201** | **2018** | **318** |
| v9.0.0 | **810** | **201** | **1949** | **301** |
| v8.1.0 | **2124** | **335** | **1854** | **277** |
| v8.0.0 | **2056** | **318** | **1792** | **262** |
| v7.0.0 | **2001** | **304** | **1738** | **249** |
| v6.0.0  | **809** | **200** | **629** | **152** |

### Constituent datasets

| Source        | beat train | beat val | binary train | binary val |
|---------------|-----------:|---------:|-------------:|-----------:|
| ballroom | 559 | 139 | 419 | 104 |
| gtzan | — | — | 258 | 63 |
| jtd | — | — | 1106 | 96 |
| rwc_classical | 49 | 12 | 32 | 7 |
| rwc_genre | 82 | 20 | 68 | 16 |
| rwc_jazz | 40 | 10 | 31 | 7 |
| rwc_popular | 80 | 20 | 80 | 19 |
| swing | — | — | 24 | 6 |
