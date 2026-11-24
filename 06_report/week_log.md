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
- Read the rulebooks: the JRC PEF guide (JRC129907), the **JRC CFB-IND battery rules** (2nd draft, June 2024), and the **GHG Protocol Product Standard** (free, ISO 14067-aligned).
- Built the **method-comparison table** (`06_report/Method_Comparison_Table.docx`): filled both rulebook columns, the "what differs & why it matters" column, and a written conclusion.
- Updated the Goal & Scope (v0.7) to match, and created an **interview-prep note** (`06_report/interview_notes.md`, 5 Q&As).

### Key decisions
- **Base case = JRC CFB-IND** (the EU battery rule). A 10 kWh home-storage battery is an "industrial battery above 2 kWh" under Reg (EU) 2023/1542, so this is the method that will legally govern its footprint from ~2027. Confirmed the battery is in scope — the "external storage" exclusion only removes flow batteries.
- **Comparison = ISO 14067**, done in practice from the **free, ISO-aligned GHG Protocol Product Standard** (ISO 14067 is paid → access via the university library).
- **Dropped Catena-X** — it is automotive-focused, and a finished home-storage battery is a different product, so it was a weak comparison. The study is now a clean two-rulebook comparison.
- **Key finding:** the JRC rule **excludes the use phase** (Art. 7 / Annex II) while ISO includes it — the biggest difference, so the ISO number is expected to be higher. The 54,000 kWh functional-unit denominator is unaffected (it is energy delivered, not emissions).

### What's still open
- [ ] Fill the actual numbers into the conclusion (JRC vs ISO result) — from Week 5+ modelling.
- [ ] Date-check the JRC rule status before finalising (still a draft).
- [ ] Confirm the few ISO 14067-specific wordings against the library copy.
- [ ] Carry the base-case recycling/electricity choices into the openLCA model (Week 3).

### Status
Week 2 complete — the method-comparison deliverable is done (filled, page-referenced, concluded). Still ahead of the 12-week plan.
