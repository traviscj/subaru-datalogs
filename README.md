# subaru-datalogs

Raw COBB Accessport (AP3, v1.7.6) datalogs from a 2012 USDM Subaru Impreza WRX
STI running a GT3076R turbo, ID1750x injectors, speed-density, flex-fuel base
tune. Each CSV is one logging session at ~30 Hz: AF correction/learning, AFR,
boost, load, timing, feedback/fine knock, DAM, injector duty, IAT, MAF, RPM,
wastegate duty, etc. The last header column carries the AP/ROM info string.

- `datalog1..5.csv` - manually triggered logs
- `datalog_automatic1..3.csv` - auto-triggered logs

Tune (`.ptm`) files are not included (proprietary format). Load the CSVs with
anything, e.g. `pandas.read_csv("datalog2.csv", encoding="latin-1")` (degree
symbols are Latin-1), or the Datazap / COBB log viewers.

License: data released under MIT.
