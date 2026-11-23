# Source Log — Inventory Data (LFP Home-Storage Battery LCA)

One row per source. Save each source's PDF/data in this `data_sources/` folder and fill in
what you pulled from it. "Data quality" is a quick gut-rating for now (High / Good / Weak) —
the proper pedigree-matrix scoring happens in Week 4.

> **Note on scope:** this project is a RESIDENTIAL / home-storage LFP battery. Prioritise the
> stationary-storage sources below. Automotive sources (GREET, IVL, Dai) are kept only to
> cross-check the **cell chemistry**, which is the same across applications.

## Primary sources — residential / stationary LFP (use these first)

| # | Source | Year | Type | What it gives | What I pulled (fill in) | Quality | Link |
|---|---|---|---|---|---|---|---|
| 1 | Le Varlet et al., "Comparative LCA of Li-ion battery chemistries for residential storage", J. Energy Storage 28 | 2020 | Paper + open dataset | **Main inventory** — residential LFP from 73 commercial modules; full material data on Mendeley | | High | Paper: https://spiral.imperial.ac.uk/bitstream/10044/1/79316/2/Revised%20Manuscript%20%28clean%29.pdf  Data: https://data.mendeley.com/datasets/stsjpkw6tm |
| 2 | Fett et al., "Life cycle GHG emissions of residential battery storage systems: A German case study", J. Industrial Ecology | 2023 | Paper (open access) | **Benchmark** — German home LFP ~210 kg CO2e/kWh (nominal); German context | | High | https://publikationen.bibliothek.kit.edu/1000154196/149925482 |
| 3 | Degen & Schutte, "LCA of the energy consumption and GHG emissions of battery cell production", J. Cleaner Production | 2022 | Paper (open access) | **Cell-factory energy** + grid effect (4.54 to 0.53 kg CO2e/kWh clean grid) | | High | https://research.chalmers.se/publication/549372/file/549372_Fulltext.pdf |
| 4 | ecoinvent — "battery, Li-ion / LiFePO4" dataset | (your version) | Database | Direct LFP battery dataset to use or compare against | | Good | In openLCA (search "battery, Li-ion") |

## Cross-check sources — cell chemistry only (automotive)

| # | Source | Year | Type | What it gives | What I pulled | Quality | Link |
|---|---|---|---|---|---|---|---|
| 5 | GREET 2023 / BatPaC 5.1 — "Li-Ion Battery Material Composition for Vehicles" | 2023 | Report | LFP cell wt.% + energy density (127-150 Wh/kg). Automotive pack — chemistry cross-check only | Composition extracted (see inventory draft) | Good | https://greet.anl.gov/files/battery_updates |
| 6 | IVL C444 — Emilsson & Dahllof, "Lithium-Ion Vehicle Battery Production – Status 2019" | 2019 | Report | Benchmark 61–106 kg CO2e/kWh (cell/production) | | Good | https://www.ivl.se (search "C444") |
| 7 | Dai, Kelly, Gaines & Wang, "LCA of Li-Ion Batteries for Automotive Applications", Batteries 5(2):48 | 2019 | Paper (open access) | Cell structure + method | | Good | https://www.mdpi.com/2313-0105/5/2/48 |

## Peer-reviewed LFP papers (add 2–3 — Google Scholar: "residential LFP battery storage life cycle assessment")

| Source | Year | Type | What it gives | What I pulled | Quality | Link |
|---|---|---|---|---|---|---|
| [Paper 1] | | Paper | | | | |
| [Paper 2] | | Paper | | | | |

## Data-quality legend
- **High** — peer-reviewed, recent (2020+), relevant to residential/stationary LFP storage
- **Good** — reputable model/report, but automotive-focused or a few years old
- **Weak** — old, generic, or indirectly relevant (use only to fill gaps)

## Reference ranges (to sanity-check your Week-5 result)
- **Cell only (production):** ~37–71 kg CO2e/kWh
- **Full home system (cell + BMS + housing):** ~200–290 kg CO2e/kWh
- Your Goal & Scope **excludes the inverter**, so expect to land a bit BELOW Fett's ~210.

## Gaps still open (fill Friday)
- [ ] Residential pack housing / enclosure mass (from Le Varlet dataset)
- [ ] Cell-factory electricity per kWh, China vs. EU (from Degen & Schutte)
- [ ] BMS / electronics mass (residential)
- [ ] End-of-life / recycling inventory
