# Box system

Originally by R3X / Scherzo; updated by MrShark45 and ftl~.

The plugin stores map boxes either in MySQL/SQLX or as JSON files. Select the mode in
[`include/box_globals.inc`](include/box_globals.inc) with `USE_SQL`:

- `1` (default): SQL storage. Import [`DB/structure.sql`](DB/structure.sql) and set the
  `SQL_*` values in `addons/amxmodx/configs/box.cfg`.
- `0`: JSON storage in `addons/amxmodx/configs/Box/<map>.json`.

SQL map names are normalized to lowercase. The database table has an index on `map` for
the load and replacement queries.
