# Procedure

1. Turn on the spectrophotometer [[GENESYS20]]

    - Allow the instrument to warm up for at least **10 minutes** if required by the manufacturer.

2. Set wavelength

    - Adjust the spectrophotometer to **640 nm**.

3. Prepare the blank

    - Fill a clean cuvette with **1 mL (or the required volume)** of **the same sterile medium** used to grow the culture.

    - Wipe the outside of the cuvette with a **lint-free tissue** to remove fingerprints or droplets.

4. Blank the instrumen

    - Insert the blank cuvette into the holder, aligning the transparent sides with the light path.

    - Close the lid and press **“Blank”** or **“Zero”**.

    - Wait until the display reads **0.000** absorbance (or 100% transmittance).

5. Measure the sample

    - Mix the microbial culture gently by inversion or pipetting (do **not** vortex to avoid cell lysis or bubbles).

    - Transfer **1 mL** of the culture into a clean cuvette.

    - Wipe the cuvette and place it in the same orientation as the blank.

    - Record the OD₆₀₀ value.

6. Dilute if necessary

    - If the OD₆₀₀ value exceeds **0.5**, dilute the sample (e.g., 1:10 in fresh medium), mix, and remeasure.

    - Multiply the measured OD₆₀₀ by the dilution factor to obtain the true OD₆₀₀.

7. Clean up

    - Rinse cuvettes thoroughly with distilled water and let them air-dry or store according to lab policy.

    - Turn off the spectrophotometer if not in continuous use.

### Notes

- Always use **the same type of cuvette** (plastic or glass) for blank and samples.

- Avoid **bubbles** and **residual droplets**—they can alter the reading.

- Record all values in a **lab notebook** or **data sheet**, including dilution factors and time points.





### 1. The origin of OD₆₀₀

- **OD₆₀₀ (600 nm)** became the **standard wavelength** for measuring bacterial growth, particularly _E. coli_, because:

    - Early **photoelectric colorimeters and spectrophotometers** (mid-20th century, e.g., Klett-Summerson colorimeter) used **filters centered around 600 nm** (“Klett filter #66” was 600 ± 20 nm).

    - At 600 nm, **visible light scattering** by bacterial cells is high, but **absorption by medium components** (especially proteins and riboflavin) is minimal.

    - It provided a convenient linear correlation between **cell density and light scattering** up to OD ≈ 0.8–1.0.

    - Consequently, OD₆₀₀ was widely adopted in bacterial growth protocols, and it became embedded in textbooks and instrument presets.




### 2. Why OD₆₄₀ (or OD₆₃₀–₆₄₀) is sometimes used

- Yeast (e.g., _Saccharomyces cerevisiae_) cells are **larger and more refractile** than bacteria; they scatter light differently.

- Early yeast researchers found that measurements at slightly **longer wavelengths (620–640 nm)**:

    - **Reduced multiple scattering** (less overestimation at high cell densities).

    - **Improved linearity** between OD and actual cell dry weight or concentration.

    - **Minimized interference** from colored media or metabolic pigments (like flavins or residual YPD coloration).

- Some instruments (especially **older spectrophotometers in yeast labs**) came equipped with a **640 nm or 620 nm filter**, not 600 nm, simply because they were originally designed for **turbidity or colorimetric assays** (e.g., McFarland standards, enzymatic reactions).

- As a result, **OD₆₄₀** became the norm in many yeast laboratories — particularly in Europe (e.g., Scandinavian and German microbiology traditions).




### 3. Practical differences

- Both wavelengths measure **scattered light**, not true absorption.

- The actual **difference in measured OD** between 600 and 640 nm is typically small (≈ 5–10%), but not negligible if one is comparing across studies.

- Empirically, some labs use correction factors:
    [
    \text{OD}_{600} ≈ 1.1 × \text{OD}_{640}
    ]
    (though this varies depending on the spectrophotometer and culture conditions).




### 4. In the literature

- _E. coli_ and most bacteria → OD₆₀₀ (historical Klett tradition, standard in molecular biology).

- _S. cerevisiae_ and other yeasts → OD₆₄₀ or OD₆₃₀ (to improve linearity with biomass and because of larger cell size/scattering behavior).

- _Microalgae_ and colored cells → even longer wavelengths (e.g., 680 nm) to minimize chlorophyll absorption overlap.




### 5. Bottom line

The difference is not biochemical, but optical and historical:

> OD₆₀₀ comes from bacterial tradition (Klett filter #66).
> OD₆₄₀ emerged from yeast work to improve scattering linearity and reduce medium interference.

Both are valid, as long as:

- You consistently use one wavelength within your lab.

- You report it explicitly (e.g., “Cell density was monitored at OD₆₄₀”) when publishing.

