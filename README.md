# Battery LFP Carbon Footprint LCA

**Battery Regulation-ready carbon footprint of an LFP home-storage battery:**
how method choice and production location change the declared result.

## Overview
A cradle-to-grave life cycle assessment (LCA) of a 10 kWh lithium-iron-phosphate (LFP)
home-storage battery, built to EU Battery Regulation / Battery Passport logic.

- **Functional unit:** 1 kWh of electricity delivered over the battery's service life
  (10 kWh x 6,000 cycles x 0.90 depth of discharge = ~54,000 kWh delivered).
- **System boundary:** cradle-to-grave, attributional (GHG Protocol 5 life-cycle stages).
- **Impact category:** climate change (GWP), IPCC GWP 100-year — kg CO2e per kWh delivered.

## Research questions
1. How much does the footprint change between ISO 14067, the JRC battery rules, and Catena-X?
2. How much do production location (China vs. EU grid), recycled content, and end-of-life change it?
3. Which levers lower the footprint most, at the lowest cost?

## Tools & data
- **openLCA** (database: `battery_lfp_lca`, copy of ecoinvent cut-off)
- **ecoinvent** (cut-off system model) — background data
- **Python** scenario pipeline (openLCA IPC) — reused from the SunPeak PV LCA project
- Foreground inventory sources: Argonne GREET, IVL (Emilsson & Dahllof 2019), Dai et al. (2019)

## Folder structure
| Folder | Contents |
|---|---|
| `01_goal_scope/` | Goal & Scope document (done) |
| `02_inventory/` | Battery bill of materials (Week 3) |
| `03_model_openlca/` | Exported openLCA models |
| `04_scenarios_python/` | Python scenario scripts (openLCA IPC) |
| `05_results/` | Result tables and charts |
| `06_report/` | Final report and dashboard |
| `data_sources/` | Source PDFs and source log |

## Status
Week 1 — Goal & Scope complete; project set up. Inventory build starts Week 3.

## Plan
12-week project, ~20 h/week. See `week1_schedule.md`.
