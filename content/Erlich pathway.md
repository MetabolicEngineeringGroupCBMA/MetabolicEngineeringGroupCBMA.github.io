---
publish: true
---

# Ehrlich pathway

The **Ehrlich pathway** converts some amino acids into **higher alcohols**, also called **fusel alcohols**. In _Saccharomyces cerevisiae_, it connects amino-acid nitrogen utilization with the formation of fermentation flavor compounds. The sequence is **transamination → decarboxylation → reduction**. It applies to several branched-chain and aromatic amino acids, and to methionine, but not to all amino acids. \[1]

## Leucine → isoamyl alcohol

![[leucine-structure.png|450]]

_Leucine: the amino group is shown in blue and the carboxyl group in red._

![[leucine-to-isoamyl-alcohol-annotated.png|900]]

_Leucine → α-ketoisocaproate → isovaleraldehyde → isoamyl alcohol (3-methylbutan-1-ol). Decarboxylation releases CO₂; aldehyde reduction consumes NADH + H⁺ and regenerates NAD⁺._

**Leucine (6 carbons) → α-ketoisocaproate (6 carbons) → 3-methylbutanal (5 carbons) → isoamyl alcohol (5 carbons).**

| Step            | Reaction                                                  | What happens?                                                                                                                         |
| --------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Transamination  | Leucine + α-ketoglutarate ⇌ α-ketoisocaproate + glutamate | The amino group is transferred to glutamate; the carbon skeleton remains. Branched-chain aminotransferases Bat1 and Bat2 participate. |
| Decarboxylation | α-Ketoisocaproate → 3-methylbutanal + CO₂                 | A decarboxylase removes one carbon as CO₂.                                                                                            |
| Reduction       | 3-Methylbutanal + NADH + H⁺ → 3-methylbutan-1-ol + NAD⁺   | An alcohol dehydrogenase reduces the aldehyde to **isoamyl alcohol**.                                                                 |

α-Ketoisocaproate is also called **4-methyl-2-oxopentanoate**; 3-methylbutanal is **isovaleraldehyde**. Isoamyl alcohol is **3-methylbutan-1-ol**, distinct from the 2-methylbutan-1-ol derived from isoleucine. Isotope-tracing experiments directly demonstrated leucine conversion to isoamyl alcohol in yeast. \[2, 3]

## The same reaction pattern as pyruvate → ethanol

![[pyruvate-to-ethanol-analogy.png|700]]

The last two steps of leucine degradation follow the same chemical pattern as **alcoholic fermentation from pyruvate**: an **α-keto acid loses CO₂ to form an aldehyde**, then the **aldehyde is reduced to an alcohol**, consuming NADH + H⁺ and regenerating NAD⁺.

| Reaction | Pyruvate → ethanol | Leucine-derived α-keto acid → isoamyl alcohol |
| --- | --- | --- |
| Starting α-keto acid | Pyruvate (3 carbons) | α-Ketoisocaproate (6 carbons) |
| Decarboxylation: release CO₂ | Pyruvate → acetaldehyde + CO₂ | α-Ketoisocaproate → isovaleraldehyde + CO₂ |
| Reduction: NADH + H⁺ → NAD⁺ | Acetaldehyde → ethanol (2 carbons) | Isovaleraldehyde → isoamyl alcohol (5 carbons) |

The carbon chain determines which alcohol is formed; **the reaction pattern is the same**. Leucine must first undergo transamination to become an α-keto acid, whereas pyruvate is already an α-keto acid when it emerges from glycolysis.

In both cases, the two illustrated steps regenerate NAD⁺ without directly producing ATP. In glucose-to-ethanol fermentation, ATP is made during **glycolysis**, before these steps. The leucine pathway instead allows amino-acid nitrogen utilization, with alcohol formation providing a possible additional route for NADH oxidation \[1].

## Why stop at an alcohol instead of completely oxidizing the amino acid?

Separate two needs: **obtaining nitrogen for biosynthesis** and **obtaining energy from carbon**.

In a sugar-containing medium, yeast can obtain carbon and energy from sugar while using leucine as a nitrogen source. Transamination captures leucine's nitrogen in glutamate, which can supply other biosynthetic reactions. Converting the remaining carbon skeleton into an excreted fusel alcohol allows nitrogen utilization without completely oxidizing that skeleton. \[3]

The reduction also consumes NADH and regenerates NAD⁺. This may contribute to redox balance during fermentation, but should not be presented as the sole reason for the pathway. It produces no ATP directly. Complete oxidation would require additional reactions and respiratory reoxidation of reduced cofactors; respiration requires oxygen. \[1]

**This is not a universal replacement for amino-acid metabolism.** Amino acids can enter proteins, and their other metabolic fates differ. Product formation also depends on conditions: aerobic, glucose-limited cultures can favour oxidation of the aldehyde to the corresponding fusel acid rather than reduction to an alcohol. \[1]

## Does all isoamyl alcohol come from supplied leucine?

No. Yeast can also generate α-ketoisocaproate through amino-acid biosynthesis from sugar-derived carbon. This intermediate can enter the alcohol-forming steps without prior breakdown of imported leucine. Thus, isoamyl alcohol production alone does not measure leucine consumption. \[3]

> **Remember:** leucine's nitrogen enters glutamate; one carbon leaves as CO₂; the other five carbons can leave as isoamyl alcohol.

## Sources

1. Hazelwood et al. (2008). [The Ehrlich pathway for fusel alcohol production: a century of research on _Saccharomyces cerevisiae_ metabolism](https://doi.org/10.1128/AEM.02625-07). _Applied and Environmental Microbiology_, 74, 2259–2266. See also the [corrected pathway figure](https://doi.org/10.1128/AEM.00934-08).
2. Dickinson et al. (1997). [A ¹³C nuclear magnetic resonance investigation of the metabolism of leucine to isoamyl alcohol in _Saccharomyces cerevisiae_](https://pubmed.ncbi.nlm.nih.gov/9341119/). _Journal of Biological Chemistry_, 272, 26871–26878.
3. Schoondermark-Stolk et al. (2005). [Bat2p is essential in _Saccharomyces cerevisiae_ for fusel alcohol production on the non-fermentable carbon source ethanol](https://doi.org/10.1016/j.femsyr.2005.02.005). _FEMS Yeast Research_, 5, 757–766.
