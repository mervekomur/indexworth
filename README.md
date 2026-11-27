# IndexWorth

**Learning what an index is worth**: a small machine-learning index advisor for PostgreSQL that predicts the latency benefit of an index *without building it*, and avoids optimizer-induced regressions.

Open the interactive dashboard: pick a database, a storage budget and an advisor to see the recommended indexes and the measured effect on the held-out test queries.

- Databases: three synthetic databases generated for this study (two sales databases with uniform and skewed distributions, one hospital-appointment schema). All timings are real measurements on PostgreSQL 16.
- Model: gradient-boosted regression trees on 31 features per query-index pair, trained leave-one-database-out.
- Selection: storage-budgeted greedy search with a regression penalty.

Author: Merve Kömür
