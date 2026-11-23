# Week 1 — "Set up & Scope" (detailed checklist)

**Project:** Battery Regulation-ready carbon footprint of an LFP home-storage battery
**Hours:** 20 h (5 days × 4 h)
**Goal of the week:** Finish a clean 2-page *Goal & Scope* document and set up the project (folders, openLCA, GitHub), ready to build the battery inventory in Week 3.

---

## Jargon, explained once

- **PCF (Product Carbon Footprint):** total CO₂ caused by one product across its life.
- **Functional unit:** the exact "one thing" you measure — here: *1 kWh of electricity delivered by the battery over its whole life*.
- **System boundary:** where the study starts and stops — here: *cradle-to-grave* (raw materials → disposal/recycling).
- **LCI (Life Cycle Inventory):** the list of everything in and out (materials, energy, emissions).
- **Foreground data:** the battery's own recipe (you collect this). **Background data:** generic materials/electricity (ecoinvent gives this).

---

## Monday — Read the two rulebooks (4 h)

Learn *what a carbon footprint study must contain* before building one.

- [ ] **Block 1 (2 h) — ISO 14067:2018:** read Clause 6 (Goal & Scope) and Clause 7 (Life Cycle Inventory); skim Clause 8 (calculating the footprint) and Clause 10 (what the report must contain).
- [ ] **Block 2 (2 h) — GHG Protocol Product Standard:** read Ch 7 (Scope) and Ch 8 (Boundary setting) carefully; skim Ch 9 (Data collection & data quality).

**Extract into a half-page "standards notes" file:**
- [ ] How each standard defines the **functional unit** and **reference flow**.
- [ ] The rules for **system boundary** (both use attributional, cradle-to-grave — that's your choice).
- [ ] The **cut-off rule** (how small a material you may ignore, usually by mass/energy %).
- [ ] What the **final report** must list (your target).

> Same job you did on your SunPeak PV module — now written up formally for a battery.

---

## Tuesday — Write the Goal & Scope (4 h)

The brain of the project. One short paragraph per section.

- [ ] **Block 1 (2 h):** draft sections 1–6.
- [ ] **Block 2 (2 h):** draft sections 7–11 + a simple boundary diagram.

**Goal & Scope template (section by section):**
- [ ] 1. **Title & author** — project title, your name, date.
- [ ] 2. **Goal** — why (research + portfolio), who for (employers/researchers), the decision it supports (how method & location change the result).
- [ ] 3. **Product description** — LFP (lithium iron phosphate) battery for home energy storage, ~10 kWh usable (fix the exact number Friday).
- [ ] 4. **Functional unit** — *1 kWh of electricity delivered over the battery's service life*; state the reference flow.
- [ ] 5. **System boundary** — cradle-to-grave; list what's IN and what's OUT.
- [ ] 6. **Life-cycle stages** — name each stage you'll model.
- [ ] 7. **Cut-off criteria** — e.g. "materials below 1% of mass excluded, except known hotspots."
- [ ] 8. **Data & quality** — background = ecoinvent (cut-off system model); foreground = published papers; quality scored with the pedigree matrix (a 1–5 scoring table from ecoinvent).
- [ ] 9. **Impact category & method** — Global Warming Potential, IPCC GWP 100-year.
- [ ] 10. **Assumptions & limitations** — write these honestly (seniors look for this).
- [ ] 11. **Rule version used** — state which battery-footprint rule version you follow and the date you checked (the EU act was delayed).

---

## Wednesday — Set up openLCA, ecoinvent, folders & GitHub (4 h)

- [ ] **Block 1 (1 h) — openLCA database:** create a new database, import ecoinvent, pick the **cut-off** system model (recycled materials come "burden-free" — the common default).
- [ ] **Block 2 (1 h) — project skeleton:** create an empty product system named `LFP_battery_basecase` as a placeholder; set the impact method to IPCC GWP 100.
- [ ] **Block 3 (1 h) — folder structure:** create the folders below.
- [ ] **Block 4 (1 h) — GitHub repo:** `git init`, add a `.gitignore` that excludes the big openLCA database files (same lesson as SunPeak), write a short README.

**Suggested folder structure:**
```
battery-lfp-lca/
├── 01_goal_scope/        ← Tuesday's doc
├── 02_inventory/         ← battery recipe (Week 3)
├── 03_model_openlca/     ← exported models
├── 04_scenarios_python/  ← reuse your SunPeak IPC pipeline
├── 05_results/
├── 06_report/
├── data_sources/         ← PDFs + source log
├── .gitignore
└── README.md
```

> Reuse the Python/openLCA IPC pipeline from SunPeak — it drops into `04_scenarios_python/` in Month 2.

---

## Thursday — Start collecting inventory sources (4 h)

Gather the **battery recipe** (the one thing ecoinvent can't give). Today = find & file the sources, not model yet.

- [ ] **Block 1 (1 h) — Argonne GREET / BatPaC (free):** cell bill of materials (cathode, anode, foils, electrolyte) + cell-factory electricity per kWh.
- [ ] **Block 2 (1 h) — IVL report, Emilsson & Dahllöf (2019):** a benchmark kg CO₂e/kWh to sanity-check your result + manufacturing energy ranges.
- [ ] **Block 3 (1 h) — Dai et al. (2019), Argonne:** detailed LFP cathode and cell material inventory.
- [ ] **Block 4 (1 h) — 2–3 peer-reviewed LFP papers (Google Scholar):** cross-check numbers; note where studies disagree.

**Output:**
- [ ] A **source log** table in `data_sources/` with columns: *Source · Year · What it gives · Rough data quality*. Save the PDFs alongside it.

---

## Friday — Write-up, finalise & decide the exact battery (4 h)

- [ ] **Block 1 (1.5 h):** tidy Tuesday's draft into a clean **2-page** Goal & Scope document; add the boundary diagram.
- [ ] **Block 2 (1 h):** fix concrete numbers — capacity (e.g. 10 kWh), cycle life (e.g. 6,000 cycles), service life → calculate total kWh delivered (sets your functional-unit denominator).
- [ ] **Block 3 (1 h):** list Week 3 data gaps from Thursday's sources.
- [ ] **Block 4 (0.5 h):** week log — one short paragraph: what you did, decisions made, what's open (your Friday habit for all 12 weeks).

---

## ✅ Week 1 deliverable

- [ ] A finished **2-page Goal & Scope document**
- [ ] Project repo set up (folders + GitHub + `.gitignore`)
- [ ] Inventory sources filed with a source log
