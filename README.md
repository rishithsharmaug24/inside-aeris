# Inside AERIS

An interactive explainer of AERIS, a research model that gives the chance that a river gauge in
Peninsular India rises above its 2-year flood flow within the next two days. It walks through the
data, the input choices, the GRU network, its training and the sealed tests, and replays the
model's real forecasts on past days (2016-2018 and August 2024 to December 2025).

Live: https://inside-aeris.vercel.app (backup: https://rishithsharmaug24.github.io/inside-aeris/)

**Research only.** AERIS issues no warnings and nothing here is fit for public-safety use. For
flood warnings in India see the India Meteorological Department (https://mausam.imd.gov.in), the
Central Water Commission (https://ffs.india-water.gov.in) and the National Disaster Management
Authority (https://ndma.gov.in).

## Files

- `index.html`: the whole page (no build step).
- `series.json`: the replay data, one series per gauge: forecast probability, outcome, river flow
  as a share of the flood flow, rain and forecast rain.

## Data credits

River flow from CAMELS-IND and the Central Water Commission via India-WRIS; rain from IMD's 0.25°
gridded data (Pai et al. 2014, MAUSAM 65); forecast rain from NOAA GEFS; weather and soil from
ERA5-Land (Copernicus); state outlines from geoBoundaries (CC BY 4.0). India-WRIS, CWC, MoWR and
IMD take no responsibility for the inferences shown here.

## Deploying

- Vercel: `npx vercel deploy --prod` from this folder (static site; `vercel.json` sets no framework).
- GitHub Pages: push to `main`; Pages serves the repository root.
