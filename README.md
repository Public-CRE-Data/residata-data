# residata-data

Weekly asking-rent, concession and net-effective-rent data for US apartment and single-family-rental REITs (AMH, AVB, CPT, EQR, ESS, INVH, MAA, UDR), updated every Sunday.

| Folder | Contents |
|---|---|
| `data/raw/` | Weekly unit-level scrapes, one CSV per REIT per week |
| `data/registry/` | Unit registry used to match the same units across weeks |
| `data/summary/` | `summary_history.csv`: weekly summary across the full history |
| `data/derived/` | Same-property indices and market comparisons (see `data/derived/README.md`) |
