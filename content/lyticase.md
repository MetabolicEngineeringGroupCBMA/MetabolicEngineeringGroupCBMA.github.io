---
publish: true
---

## Purification of lyticase

The strain `µ761` is likely an _E. coli_ DH5alfa carrying the pUV5-G1S vector.  This vector expresses the beta-1,3-glucanase from _Oerskovia xanthineolytica_
from the [[lacUV5]] promoter.

Karl Kuchler sent me the E. coli strain after the 2004 Yeast Genetics & Molecular Biology Meeting in Seattle.

The plasmid pUV5-G1S was constructed by cloning of the gene into the plasmid pOP95-15 at its unique EcoRI site, described in Shen 1991.  The plasmid pOP95-15 was constructed in (Fuller 1982).

The recombinant lyticase has been used in literature:

"Vacuoles were isolated through hydrolysing yeast cell walls using lyticase, recombinantly expressed in Escherichia coli RSB805 (provided Dr. Randy
Schekman, Berkeley), and were prepared from a periplasmic supernatant."

in Alpadi 2013, they also offer a detailed protocol

---

Shen, S. H., Chrétien, P., Bastien, L., & Slilaty, S. N. (1991). Primary sequence of the glucanase gene from Oerskovia xanthineolytica. Expression and purification of the enzyme from Escherichia coli. _J. Biol. Chem._, _266_(2), 1058–1063. <https://www.ncbi.nlm.nih.gov/pubmed/1985933>

Alpadi, K., Kulkarni, A., Namjoshi, S., Srinivasan, S., Sippel, K. H., Ayscough, K., Zieger, M., Schmidt, A., Mayer, A., Evangelista, M., Quiocho, F. A., & Peters, C. (2013). Dynamin-SNARE interactions control trans-SNARE formation in intracellular membrane fusion. _Nat. Commun._, _4_, 1704. <https://doi.org/10.1038/ncomms2724>

"Vacuoles were isolated through hydrolysing yeast cell walls using lyticase, recombinantly expressed in Escherichia coli RSB805 (provided Dr. Randy
Schekman, Berkeley), and were prepared from a periplasmic supernatant."

Fuller, F. (1982). A family of cloning vectors containing the \_lac\_UV5 promoter. _Gene_, _19_(1), 43–54. <https://doi.org/10.1016/0378-1119(82)90187-1>

---

The original protocol as a word file sent to me by Karl Kuchler: [[Protocol_041007_lyticase_prep_from_ecoli.doc]]

## Prep work:

Plate RSB805 (µ761) on solid LB medium with ampicillin 37°C.
Inoculate and grow to stationary phase (for example o/n) in liquid LB medium with ampicillin.
Inoculate fresh LB medium with ampicillin  with stationary culture ; 1/100 dilution is good. even 1/200 is OK, doubling time for this strain is 40 minutes
Grow until 0.5 OD640, then induce by adding IPTG to 0.4 mM
Grow for another 5 hours
Harvest cells by centrifuging in 50 mL FALCON tubes,
Wash with 25 mM Tris pH 7.4.
Resuspend cells in 1/50 original volume in 25 mM Tris pH 7.4; add EDTA to 2 mM final concentration.
Add equal volume of 40% sucrose, 25 mM Tris pH 7.4; mix gently for 20 minutes and no longer!
Spin cells in GSA at 7,500rpm for 10 minutes. For good "shocking", make sure that all sucrose buffer is removed.
Resuspend cells with no more than 1/50 original volume in ICE COLD 0.5 mM MgSO4; mix gently: 20 minutes on ice
Spin cells in SS34 at 10,000 rpm for 10 minutes

## Make assay cells:

grow desired WT yeast cells to OD640<1  (cells do not spheroplast well at higher OD!) harvest cells and wash with dH20 resuspend cells in 50 mM Tris pH 7.4 to OD640 = 5.

## Optional purification:

We normally use crude shock fluid unless purified lyticase is especially desired. To store crude shock fluid (i.e. the supernatant from the prep work, without dialysis or pH adjustment),
aliquot and quick freeze in liquid nitrogen and store at -80C.

We have not noticed a significant decrease in activity after prolonged storage. It may be a good idea to add azide to the shock fluid after thawing to avoid contamination.

Transfer the supernatant containing the lyticase to dialysis tubes and dialyze against 50mM NaOAc pH 5.0

1. Batch bind dialyzed supernatant to CM Sepharose which has been pre-equilibrated in 50mM NaOAc pH5.0. 	Load bound mix onto fat short column (save the flowthrough just in case...)
2. Wash the column with 50mM NaOAc pH5.O (2-3x column volume)
3. Elute lyticase with 150mM NaCl, 50mM NaOAc pH5.0. Flow rate should be ~7ml/minute and collect 7ml fractions. General rule of thumb: lyticase will start to elute just after one column volume of elution buffer has gone through
4. Monitor every fifth fraction for activity then assay every other fraction across the peak. combine the peak fractions.

Assay:

Make fresh 2x buffer:

- 100 mM Tris-HCl pH 7.4,
- 80 mM 2-ME

One 15 mL FALCON tube for each assay point:

- 1000 µl 2x assay buffer
- 920 µl ddH2O
- 80 µl cells (final OD640 is about 0.2)
- 0 - 50 µl 	collected fractions

Remove 1 ml and measure OD640 for "zero" point. Incubate remainder at 30°C for 30 minutes then determine OD640; 	1 unit = 10% decrease in OD640 after 30 minutes at 30°C
