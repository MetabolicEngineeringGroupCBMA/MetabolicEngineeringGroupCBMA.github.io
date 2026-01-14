## Yeast two-hybrid library screen by mating




http://protocols.mmml.nl/protocols/yeast/Y2H_mating.php



This protocol assumes using yeast strains Y8800/Y8930. If using a different strains, adapt 3-AT concentrations and/or phenotypic assays.

Library Generation

The first step is to generate a frozen library of AD-fusions in Y8800 (the mating type used for AD and DB plasmids does not matter, but the convention in the Vidal lab is to put AD plasmids in MATa strains). Follow the liquid transformation protocol to make Y8800 competent. Then transform an AD library. The total frozen library size is determined by how much AD-library is transformed. This protocol is based on 30 µg of library plated on 30 plates (15cm diameter), which yields between 1x106 and 2x106 colonies.

In a 15 ml falcon tube, mix the following:
1.6 ml competent yeast cells
160 µl boiled salmon sperm DNA
30 µg AD-library
fill up to 9 ml with TE/LiAc/PEG
Aliquot the 9 ml into 1 ml eppendorf tubes.
Incubate all eppendorf tubes at 30°C for 30 min.
Incubate all eppendorf tubes at 42°C for 15 min.
Spin in microfuge for 5 sec.
Resuspend pellets in 1 ml H2O and pool the yeast.
Plate 300 µl of the final mixtures onto 30 -Trp plates.
Also plate 300 µl of a 1:1000 dilution onto a -Trp plate to determine the total number of transformants.
After growing the colonies for 2 days, harvest all the yeast by washing the colonies of the plates with YEPD using a 10 ml pipette. 10-15 ml of YEPD per plate works well. After collecting the yeast, add 20% glycerol and freeze 1-2ml aliquots in a -80° freezer. Measure the OD600 of the library. OD600 values are not linearly correlated with yeast density, and the amount of cells used below is based on a measured OD600 lower than 1. The library will likely need to be diluted 10x in YEPD before measuring to achieve this.

Y2H Screening

The amounts of yeast and plates used depend on the number of colonies to be screened. This protocol is based on screening between 1x106 and 3x106 diploid yeast, but the protocol is easily scaleable.

Day 1

Grow DB-bait in Y8930 yeast O/N in 10 ml YEPD in a 50 ml falcon tube. Measure the OD600 of a 10x dilution. This will usually be around 0.5, giving an OD600 of 5 per ml of O/N culture.
Thaw an aliquot of AD-library in Y8800, and dilute in YEPD to a final OD600 of 3 per ml of diluted yeast.
In a 2ml tube, mix 3OD of each yeast. If all went well, this means 1ml of AD-library and 0.6 ml of DB-bait strain.
Spin 30 sec. at 5000 rpm, and resuspend in 300 µl water.
Plate yeast on a 10 cm YEPD plate.
Incubate at 30°C for 4 hours. This is long enough for mating to occur, and hopefully short enough to prevent mating + subsequent divisions. The mating efficiency is about 1%.
Wash the yeast off the plate with 2 ml of water, using a P1000 pipette. Collect the yeast in a 2 ml tube.
Spin 30 sec. at 5000 rpm, and resuspend in 300 µl water for each selection plate.
Plate the yeast on 15 cm -Leu -Trp -His (+3-AT) plates. One plate is often sufficient for a cDNA library screen, more plates can be used if positives start to crowd each other. Addition of 3-AT is usually not necessary, but up to 5 mM can be used if too much background is observed.
Also plate a 1:10,000 dilution on a -Leu -Trp plate to calculate the number of diploids screened. Incubate all plates at 30°C.
Day 3

Count the number of colonies on the control plate, and calculate the number of diploids screened. This should be between 1x106 and 3x106 diploid yeast.
Day 4-5

Pick positive colonies into ~25 µl of water. From this, spot 5 µl onto 2 -Leu -Trp -His plates.
Day 6

Replica plate one of the -Leu -Trp -His plates to phenotype assay plates. For Y8800/Y8930 these are:
-Leu -Trp -His +2mM 3-AT. A little 3-AT gives better distinction between weak and strong interactors than no 3-AT at all.
-Leu -Trp -Ade. The ADE2 reporter is more stringent than the HIS3 reporter for most interactions.
-Leu -His + 1µg/ml cycloheximide. Anything that grows does so without the AD plasmid, and is thus a false-positve.
-Leu -Trp plate for X-gal assay if you'd like to do this assay too (it is not particularly pretty or informing with the Y8800/Y8930 strains).
Use the other -Leu -Trp -His plate for lysis and glycerol stocks. A common source of false positives is yeast cells that contain more than one AD plasmid. A method to eliminate these is described in Vidalain, Boxem et. al. However, with the mating method, this appears to be much less common. Thus, the yeast can be used for lysis and PCR without further processing.
Resuspend the yeast in 30 µl lysis buffer lacking the zymolyase.
Add 10 µl of the yeast to ~100 µl YEPD with 20% glycerol and freeze at -80°C.
To the remaining 20 µl of yeast, add 20 µl of lysis mixture with 2x the normal zymolyase concentration. Lyse as usual and use 2 µl for PCR.
Day 8

Score the phenotype plates. For X-gal assay, Y8800 and Y8930 need to be tested using an agar overlay essay.
