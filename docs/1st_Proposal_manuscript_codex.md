# Proposal Presentation Manuscript

## Working title

**AIS Track-Based Analysis of Port Approach Traffic and Prioritization of Monitoring Areas**

**Study area:** Norfolk and Hampton Roads, Virginia, USA  
**Course:** Special Topics in Naval Architecture  
**Team:** 고영조 · 김희선 · 백지원 · 조민제

> This is a proposal-stage manuscript. Bracketed items are deliberate placeholders for information that must come from data analysis, team decisions, or final slide design. Do not replace them with estimates before the analysis is complete.

---

## Slide 1 — Title

### On-slide text

**AIS Track-Based Analysis of Port Approach Traffic and Prioritization of Monitoring Areas**

Norfolk and Hampton Roads, Virginia, USA  
Special Topics in Naval Architecture · 2026  
고영조 · 김희선 · 백지원 · 조민제

### Visual direction

Use a restrained AIS track image or a map of the study area as the background. Keep the title legible and avoid implying that the map represents completed analysis.

---

## Slide 2 — Team

### On-slide text

**Project team**

| Team member | Role / contribution |
| --- | --- |
| 고영조 | [To be assigned] |
| 김희선 | [To be assigned] |
| 백지원 | [To be assigned] |
| 조민제 | [To be assigned] |

### Speaker notes

Introduce the team and briefly describe each member's project responsibility once the roles have been agreed. Avoid assigning roles before the team confirms them.

### Visual placeholder

`[PLACEHOLDER: team photos, affiliations, or one-line introductions, if desired]`

---

## Slide 3 — Problem and Motivation

### Headline

**Where should limited monitoring resources be focused around a busy port approach?**

### On-slide text

- Port approaches are shared by vessels with different operating patterns.
- Monitoring capacity is limited, so managers need evidence about where and when traffic is concentrated.
- AIS tracks can describe observed vessel movements and differences in spatial use over time.
- This study will use those patterns to identify candidate areas for closer monitoring.

### Speaker notes

Norfolk and Hampton Roads are the initial study area. The project will examine the spatial and monthly patterns of cargo vessels and tankers, then assess whether candidate monitoring areas remain similar when the grid size and selection threshold change. The goal is to provide a transparent basis for reviewing monitoring priorities, rather than to claim that AIS tracks alone measure safety risk.

### Visual placeholder

`[PLACEHOLDER: locator map showing the U.S. East Coast and the Norfolk / Hampton Roads study area]`

---

## Slide 4 — Research Questions and Workflow

### Research questions

1. Where are observed vessels concentrated within the port approach area?
2. How do cargo-vessel and tanker use areas overlap, and how do their patterns vary by month?
3. Do candidate monitoring areas remain similar when grid size and selection threshold change?

### Workflow

**Acquire data → Inspect and filter → Define study area and project coordinates → Aggregate tracks to grids → Compare vessel groups and months → Test selection stability → Present candidate areas and evidence**

### Preliminary team responsibilities

| Workstream | Owner |
| --- | --- |
| Data acquisition and metadata review | [To be assigned] |
| Study-area boundary and spatial preprocessing | [To be assigned] |
| Traffic statistics and sensitivity analysis | [To be assigned] |
| Maps, manuscript, and final review | [To be assigned] |

### Visual placeholder

`[PLACEHOLDER: workflow diagram; update the role table after team agreement]`

---

## Slide 5 — AIS Data Overview

### On-slide text

- **Primary source:** NOAA Office for Coastal Management, *AIS Vessel Tracks 2024*.
- **Study period:** January–December 2024.
- **Initial study area:** Norfolk / Hampton Roads port approaches.
- **Initial vessel groups:** cargo vessels and tankers, subject to verification against the source classification.
- **Fields to review:** track geometry, MMSI, track start and end times, and vessel group/type.

### Results to insert after data inspection

| Data check | Result |
| --- | --- |
| Source file format and structure | `[TO BE FILLED AFTER INSPECTION]` |
| Rows / features and columns / fields | `[TO BE FILLED AFTER INSPECTION]` |
| Records within the study area | `[TO BE FILLED AFTER SPATIAL FILTERING]` |
| Missing values in key fields | `[TO BE FILLED AFTER DATA QUALITY REVIEW]` |
| Cargo-vessel and tanker records / unique MMSIs | `[TO BE FILLED AFTER CLASSIFICATION REVIEW]` |

### Figure placeholders

- `[PLACEHOLDER: chart of records by vessel group, including unknown or other groups if useful]`
- `[PLACEHOLDER: map preview of raw tracks in and around the study area]`

### Speaker notes

Report the file format and counts only after inspecting the downloaded data. Distinguish track records from unique MMSIs: one vessel may contribute multiple tracks. State whether statistics describe the full source or only the spatially filtered study-area subset.

---

## Slide 6 — Data Preparation and Analysis Design

### Planned preparation steps

1. Review source metadata, fields, coordinate reference system, and time convention.
2. Check missing or invalid MMSI, vessel-group, time, and geometry values; document duplicate and implausible records.
3. Confirm a navigationally meaningful study boundary for the Norfolk / Hampton Roads approaches.
4. Select a suitable local projected coordinate reference system for distance- and area-based operations.
5. Retain tracks that intersect the study boundary and prepare a regional analysis dataset.
6. Create a 500 m grid for the primary analysis; repeat the analysis at 250 m and 1 km.
7. Summarize track counts and unique MMSIs separately, by vessel group and track-start month.

### Primary selection design

- **Primary grid size:** 500 m
- **Primary selection threshold:** top 10% of occupied grid cells by unique MMSI count
- **Sensitivity settings:** 250 m, 500 m, and 1 km grids; top 10% and top 20% thresholds
- **Comparison:** assess overlap and location changes using a common spatial reference

### Decisions / results to insert

- Study boundary source and version: `[TO BE CONFIRMED]`
- Projected coordinate reference system: `[TO BE CONFIRMED]`
- Vessel-group field values mapped to cargo and tanker: `[TO BE CONFIRMED AFTER INSPECTION]`
- Final inclusion and quality-control rules: `[TO BE DOCUMENTED AFTER REVIEW]`

### Figure placeholder

`[PLACEHOLDER: study boundary and example 500 m grid overlaid on a small sample of tracks]`

---

## Slide 7 — Planned Outputs, Potential Use, and Limits

### Planned outputs

- Vessel-group track maps and monthly traffic summaries.
- Grid-level counts of tracks and unique MMSIs, reported separately.
- Candidate monitoring-area map and a table explaining the selection criteria.
- Sensitivity comparison showing how candidate areas change across grid sizes and thresholds.

### Potential use

The resulting maps and summaries may help port or maritime managers review where monitoring coverage could be prioritized. Areas with persistent observed traffic may also be useful when planning follow-up surveys or maintenance reviews, in combination with appropriate infrastructure and hydrographic information.

### Interpretation limits

- AIS reception gaps and track-building rules can omit or split vessel movements.
- A track count is not an arrival count, and repeated tracks from one vessel are not independent vessels.
- Spatial overlap between routes does not establish that vessels met or faced a collision risk.
- AIS track patterns alone cannot identify “ghost ships,” illegal activity, or infrastructure condition. Those assessments require independent data and validation.

### Results placeholders

- Main observed concentration pattern: `[TO BE FILLED AFTER ANALYSIS]`
- Cargo / tanker comparison: `[TO BE FILLED AFTER ANALYSIS]`
- Stability of candidate areas across sensitivity settings: `[TO BE FILLED AFTER ANALYSIS]`

### Figure placeholders

- `[PLACEHOLDER: final monitoring-candidate map]`
- `[PLACEHOLDER: sensitivity comparison chart or map]`

---

## Slide 8 — Selected References

1. NOAA Office for Coastal Management. *AIS Vessel Tracks 2024*. Dataset metadata: <https://www.fisheries.noaa.gov/inport/item/75937>. Data index: <https://ocmgeodatastor1.blob.core.windows.net/marinecadastre/ais/aistrack/index-aistrack.html>.
2. NOAA Office for Coastal Management. *Automatic Identification System (AIS) Frequently Asked Questions*. <https://coast.noaa.gov/data/marinecadastre/ais/faq.pdf>.
3. NOAA Office of Coast Survey. *NOAA Electronic Navigational Charts*. Use the applicable chart and edition selected for the study-area boundary.

> Confirm the exact chart product, edition, access date, and final dataset citation before presenting the completed study.
