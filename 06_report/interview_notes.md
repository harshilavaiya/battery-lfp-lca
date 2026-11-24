# Interview Prep — LFP Battery LCA Project

Ready-to-say answers for questions about this project. Keep adding Q&As as they come up.

---

## Q1. Why did you choose the JRC battery rules (CFB-IND) as your base case, and the others as comparisons?

**Say:** "A home-storage battery is classed as an *industrial battery* under the EU Battery Regulation, so the JRC CFB rules are the method that will legally govern its declared footprint from 2027. My base-case number is therefore the one a manufacturer would actually have to declare — which makes the study realistic, not academic. I then compared it against ISO 14067 — the general international standard — to measure how much the declared footprint changes with the rulebook."

- JRC = **legally binding** for this product → the base case should be the number actually required.
- ISO 14067 = the established, flexible general standard → shows how the number differs from the strict new EU rule.
- Matches the project title: *"Battery Regulation-ready."*

---

## Q2. If JRC already fits your battery perfectly, why compare it to ISO 14067 at all?

**Say:** "Because the comparison *is* my research. From 2027 the EU legally forces battery makers to declare a carbon footprint using the new JRC rules — but that rule is brand new, still in draft, and nobody has publicly shown how its number differs from the established method (ISO 14067) that industry already trusts. My project is the first to measure that gap for a home-storage LFP battery, before the rule becomes mandatory. A single JRC number tells me nothing about how robust it is; comparing shows how much the declared footprint changes with the method — and why (for example, JRC excludes the use phase while ISO 14067 includes it)."

Reasons:
1. The comparison quantifies the **method effect** — how much of the number is real versus an artefact of the rulebook.
2. It is **novel and timely**: the EU rule is being finalised now, the Battery Passport is mandatory from Feb 2027, and no public study has done this for home storage.
3. It is **decision-useful**: it tells manufacturers what number to expect and shows regulators where the new rule behaves unexpectedly (e.g. excluding the use phase).
4. ISO 14067 is the **established, stable yardstick**; the JRC rule is still a draft, so the comparison shows how sensitive the result is to the method.

**One-liner:** "JRC tells me what my battery's footprint IS; the comparison tells me how much that number can MOVE versus the established standard, and why."

---

## Q3. Is your battery actually in scope of the CFB-IND rules? (title says "industrial batteries above 2 kWh, excluding those with exclusively external storage")

**Say:** "Yes. My battery qualifies as an industrial battery above 2 kWh under the CFB-IND rules. The 'external storage' exclusion only removes flow batteries — which store energy in external liquid tanks — whereas mine stores energy inside the cells."

Checklist: rechargeable ✓ | industrial (= stationary/home storage) ✓ | above 2 kWh (10 kWh) ✓ | energy stored in cells, not external tanks ✓

---

## Q4. How did you apply ISO 14067 if it's a paid standard you don't own?

**Say:** "ISO 14067 is a paid standard, so I accessed it through my university library (DIN/Perinorm) — the normal way practitioners get standards, through an institution, not by buying them personally. I also used the free GHG Protocol Product Standard, which is deliberately aligned with ISO 14067 and requires the same things, as the practical basis for the modelling. What matters for the comparison is the key methodological choices — functional unit, cradle-to-grave boundary, use-phase inclusion, allocation and data quality — and those are well documented and publicly available."

- Interviewers test your **understanding** of the standard, not whether you own the PDF.
- Proper access routes: **university library** (DIN / Perinorm / Nautos), an **employer**, or the **free, ISO-aligned GHG Protocol Product Standard**.
- In the study, that column is labelled **"ISO 14067 / GHG Protocol (general standard)"**, and the modelling is done from the free GHG Protocol.

---

## Q5. Why does this comparison matter right now? (the "today vs 2027" story — good opener)

**Say:** "Right now there's no single mandatory method — manufacturers calculate carbon footprints voluntarily, and ISO 14067 is the established standard they use. But the EU Battery Regulation is turning this into a legal requirement, calculated with the EU's own JRC rules: the Digital Battery Passport becomes mandatory in February 2027 for industrial batteries over 2 kWh and must contain the carbon footprint, with the declaration obligation phasing in around 2027–2028. So the industry is moving from a voluntary 'ISO 14067 world' to a mandatory 'EU JRC-rule world', and my project measures how much the declared number changes in that switch — before companies are forced to make it. That's why my two columns are exactly 'what manufacturers use now' versus 'what the law will force them to use'."

- **Today:** voluntary; ISO 14067 / GHG Protocol are the common choices.
- **~2027–2028:** mandatory under the EU Battery Regulation, using the JRC CFB rules; Battery Passport mandatory 18 Feb 2027.
- **Accuracy tip:** say "around 2027" (the industrial-battery rule is still being finalised) — the caveat makes you look more informed.

---

## Key technical points to have ready

- **Use phase:** the JRC rule **excludes** the use phase (Art. 7 / Annex II, Reg (EU) 2023/1542); ISO 14067 can include it (cradle-to-grave). *"Whether the use phase counts"* is itself one of my findings.
- **Functional unit:** 1 kWh delivered over service life (10 kWh x 6,000 cycles x 0.90 = 54,000 kWh). This denominator is the energy delivered (the function), so it is **unaffected** by the boundary choice — excluding the use phase only removes use-phase emissions from the numerator.
- **Main hotspot:** materials + cell manufacturing (~70-85% in published LFP studies); biggest lever = cell-factory electricity → the China-vs-Germany scenario.
- **Electricity rule (JRC):** supplier dataset if DQR <=2, else the country average electricity consumption mix — this is the China-vs-Germany lever, defined in the rule.
- **Benchmark:** full residential LFP system ~200-290 kg CO2e/kWh (Fett 2023 ~210); cell-only ~37-71 kg CO2e/kWh.
