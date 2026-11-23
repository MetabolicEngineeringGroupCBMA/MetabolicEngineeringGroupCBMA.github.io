---
publish: true
---

Amplifying fragments **greater than 5–10 kb** pushes the standard PCR protocol. Longer amplicons increase the chance of premature termination, template
nicking/damage, secondary structure stalling, and (for non-proofreading enzymes) accumulated base misincorporations.

## Polymerase Comparison (Lab Toolkit)

| Feature                      | Homemade Taq                         | Accuzyme                                               | Q5 High-Fidelity                            |
| :--------------------------- | :----------------------------------- | :----------------------------------------------------- | :------------------------------------------ |
| **Proofreading (3'→5' exo)** | No                                   | Yes                                                    | Yes                                         |
| **Amplicon Ends**            | 3' A-overhangs                       | Blunt                                                  | Blunt                                       |
| **Typical Sweet Spot**       | Up to ~2–4 kb (solo)                 | Up to ~5 kb                                            | Up to 10 kb (complex) / 20 kb (simple)      |
| **Extension Rate (Long)**    | ~60 s/kb                             | ~30 s/kb                                               | 20–30 s/kb (40–50 s/kb above 6 kb)          |
| **Best Use for 5–10+ kb**    | Only as base in a proofreading blend | Routine cloning up to ~5 kb; push carefully above 5 kb | Primary choice for 5–10+ kb & high fidelity |

> [!tip] Practical Rule of Thumb
>
> - **5–10+ kb with high accuracy or tricky GC/AT content:** Start with **Q5**.
> - **Up to ~5 kb (or occasional stretch to 6–7 kb on clean plasmid/amplicon):** **Accuzyme** is fast and reliable.
> - **Homemade Taq alone:** Generally unreliable past ~3–4 kb because a single misincorporated base can stall extension and cause truncated smears.

## Cycling Guidelines for 5–10+ kb

### 1. Q5 High-Fidelity (Recommended for 5–10+ kb)

- **Initial denaturation:** 98 °C for 30 s
- **Cycling (25–35 cycles; keep cycles on the lower end for long targets to minimize errors/chimeras):**
  - **Denature:** 98 °C for 10 s
  - **Anneal:** Primer-specific (check NEB $T_m$ calculator; 15–30 s)
  - **Extend:** 72 °C at **30–50 s/kb** (use ~30 s/kb up to 5–6 kb, and step up to **40–50 s/kb** for targets **greater than 6 kb** or GC-rich regions)
- **Final extension:** 72 °C for 2–5 min

### 2. Accuzyme

- Follow supplier buffer/$\text{Mg}^{2+}$ guidance.
- **Extension:** Start around **30–45 s/kb** at 68–72 °C and extend final extension to 5–10 min when pushing toward or past 5 kb.

### 3. Homemade Taq

- Lower extension temperature slightly (e.g., **68 °C** instead of 72 °C) can help reduce secondary structure and improve read-through on long templates.
- Plan for **~60 s/kb** extension time and avoid excessive cycle counts (stay around 25–30 cycles if template concentration allows).

## Critical Factors That Make or Break Long PCR

1. **Template Integrity First:** Sheared, degraded, or UV/freeze-thaw-damaged genomic DNA breaks before the polymerase finishes a 10 kb run. Check gDNA on a low-percentage agarose gel (e.g., 0.6–0.8%) before blaming the PCR.
2. **Avoid Over-Inputting Template:** Too much gDNA introduces inhibitors and nonspecific priming sites; too much plasmid increases off-target recombination/smears. Titrate down if you see background smears.
3. **Primer Design:** Aim for 22–30 nt primers
4. **Additives for Secondary Structure:** For GC-rich or stubborn 5–10 kb targets, test Q5 High GC Enhancer or a low titration of DMSO (typically 2–5%).
5. **Gel Electrophoresis:** Use a **0.6–0.8% agarose gel** run slowly at lower electric field so 5–10+ kb bands separate cleanly and don't compress near the top.
