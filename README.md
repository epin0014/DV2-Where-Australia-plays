# Where Australia Plays

FIT3179 Data Visualisation 2 (Monash University, Semester 2 2026) by Emilio Pinelo Landarte.

Who moves, what Australians play, and the Barassi Line that still splits the country's football. Built with Vega-Lite.

## Structure

- `index.html`: the page. The layout uses the Pure.css grid (`pure-g` / `pure-u-*`).
- `css/style.css`: fonts, colours and spacing.
- `js/main.js`: embeds each chart in its `div` with `vegaEmbed`.
- `specs/`: one Vega-Lite JSON spec per chart (11 charts, 4 of them maps). Each spec has its own `config` block for fonts and sizes.
- `data/`: the data files the charts read (see below).
- `sketch/DV2_sketch.pdf`: the hand-drawn design sketch.

## Data files

Cleaned source data:

- `ausplay_organised_2025.csv`: organised vs informal participation by age and sex (population pyramid).
- `ausplay_activity_state_2025.csv`: participation in each activity by state (proportional symbol map).
- `osm_pitches_au.csv`: Australian football and rugby league grounds (dot map).
- `australia_states.topojson`, `state_centroids.csv`: state boundaries and label positions (all maps).

Chart tables, made from the cleaned AusPlay data with `make_chart_tables.py` (one small table per chart):

- `waffle_squares.csv`, `gender_gap.csv`, `heatmap_age_activity.csv`, `bump_ranks.csv`, `activity_change.csv`, `slope_states.csv`, `state_weekly_2025.csv`, `football_share.csv`.

## Sources

- AusPlay data tables, Australian Sports Commission, January–December 2025 (released 30 April 2026), plus calendar-year national tables for 2017–2022 and 2024.
- Australian football and rugby league grounds © OpenStreetMap contributors (ODbL), extracted 9 October 2026 via the Overpass API.
- State and territory boundaries: ABS ASGS Edition 3 (2021), CC BY 4.0, simplified with mapshaper.

Generative AI (Claude) assisted with the data cleaning scripts and text editing.
