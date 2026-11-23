# Project Log — LFP Home-Storage Battery LCA

A short dated entry each week: what I did, decisions made, what's open.
(Friday habit for all 12 weeks.)

---

## Week 1 — "Set up & Scope"
**Dates:** ______ to ______

### What I did
- Defined the **Goal & Scope** (2-page document): product = 10 kWh residential LFP battery;
  functional unit = **1 kWh delivered over service life**; cradle-to-grave, attributional;
  impact = IPCC GWP 100.
- Built the **system boundary diagram** using the GHG Protocol's 5 life-cycle stages
  (material acquisition / production / distribution / use / end-of-life); inverter excluded.
- Set up the project: folder structure, openLCA working database (`battery_lfp_lca`,
  ecoinvent cut-off), and a **GitHub repo** (github.com/harshilavaiya/battery-lfp-lca).
- Collected and logged **sources**, switching from automotive data to proper
  **residential/stationary LFP** sources.
- Started the **inventory early**: built an industry-style LCI spreadsheet (bill of materials,
  factory energy, benchmarks, clickable sources) from the Le Varlet (2020) dataset.

### Key decisions
- **Reference battery:** 10 kWh usable, 6,000 cycles, 0.90 DoD → **54,000 kWh** delivered over life.
- **Main inventory source:** Le Varlet et al. (2020) residential LFP (8.1 kWh usable system),
  scaled to 10 kWh. Its specs (~5,866 cycles, 0.88 DoD) closely match my assumptions — good justification.
- **Excluded the inverter** from the system boundary (keeps focus on the battery).
- **System model:** ecoinvent cut-off.
- **Benchmark to aim near:** full residential LFP system ~200–290 kg CO2e/kWh (Fett 2023 ~210);
  expect to land slightly below because the inverter is excluded.

### What's still open (for Week 3 / 4)
- [ ] Confirm each **ecoinvent dataset** in the inventory's "Suggested" column.
- [ ] Choose the **cell-factory electricity** base value (range 9–63 kWh/kWh).
- [ ] Collect **end-of-life / recycling** data.
- [ ] Decide the **base-case grid** (China vs. Germany vs. EU).
- [ ] Score **data quality** with the pedigree matrix (Week 4).
- [ ] Add name + date to the Goal & Scope cover.

### Status
Week 1 complete — and ahead: Goal & Scope done, project on GitHub, sources logged,
and the inventory already drafted (normally Week 3 work).

---

## Week 2 — "Read the rulebooks"
**Dates:** ______ to ______

### What I did
-

### Key decisions
-

### What's still open
-
