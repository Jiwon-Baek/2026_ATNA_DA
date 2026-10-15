# Raw data

Place downloaded NOAA AIS source archives here. Large source data is intentionally kept out of version control. Record the source URL, download date, archive name, and checksum in the project notes when downloading.

The source is NOAA's nationwide `AISVesselTracks2024.zip` archive (about 6.81 GiB according to the official index). Downloaded on 2026-10-15; the archive contains `AISVesselTracks2024.gpkg`. The original archive is kept here and ignored by version control. It is available from:

- <https://ocmgeodatastor1.blob.core.windows.net/marinecadastre/ais/aistrack/AISVesselTracks2024.zip>

Before analysis, inspect the GeoPackage layer names, CRS, fields, and counts. Extract or spatially filter to the regional study area before loading data into memory; place derived data in `data/interim/` and `data/processed/`.
