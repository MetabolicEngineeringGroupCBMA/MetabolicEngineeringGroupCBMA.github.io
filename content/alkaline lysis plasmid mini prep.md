# Low cost E. coli plasmid alkaline lysis mini-prep

Also known as (Snik-protokollet från [TMB](http://www.tmb.lth.se)).

This protocol can be used to prepare plasmid DNA from cells in liquid culture or growing on solid medium.
Cells from fresh o/n cultures tend to give the best results.
If cultures can not be processed right away, pelleted cells can be stored a -20°C for future plasmid preparation.
For solid medium, we have found that it might be better to scrape cells off the plate, wash with P1 and save the
pellet at -20°C rather than saving the plate in the fridge for several days as cells on plate tend to become slimy after a while.

Any microcentrifuge can be used for this protocol, the maximum force generated seems not to be critical.

Picofuge type centrifuges may **not** give sufficient force to pellet precipitated DNA, but is fine for spinning cells.

![pico](pico.jpeg)


## Collect cells from liquid culture

1. Grow 1 ml of *E. coli* in a 1.5 - 2 ml Eppendorf tube at 37°C o/n. Larger 2 mL tubes might be better, since mixing seems more efficient. Tubes can be incubated sideways at 200 rpm.

2. Centrifuge at top speed for 30 s to recover cells.

3. Resuspend cells in 200 µL of buffer P1. Cells can be vortexed briefly or cells can be resuspended by pipetting up and down with a P1000 pipette.

## Collect cells from solid culture

1. Streak about a quarter to a half of a LB plate necessary antibiotic from a colony or directly from a frezer stock and incubate o/n.

2. On the next day, collect cells from at least 1/4 of the inoculated solid medium using a toothpick with a flat end.

3. Resuspend the cells in 200 µL buffer P1. If the cells are hard to resuspend, try to decant as much as possible of the cells to another tube and leave behind the sticky biomass..


## Alkaline lysis

4. Add 200 µL of buffer P2, mix by inversion about ten times, **do not vortex** or else the chromosomal DNA might fragment and contaminate the plasmid DNA. **Wear goggles for this step!**

5. Incubate at room temperature for 3-5 min. **Do not incubate more than 5 min**, keep the time with you cell phone or clock. If possible slowly invert the tube during the entire incubation.

## Neutralization

6. Add 250 µL buffer P3, mix by inversion about ten times, **do not vortex** for the same reason as before.

7. Centrifuge at top speed for 5-10 min. While centrifuge is running, add 1 ml of 96% - 99,5% ethanol
   to a new clean 1.5 ml Eppendorf tube for each plasmid prep. 750 µL of Isopropanol can be used instead of ethanol.

## Ethanol precipitation

8. Add 500 µL of the supernatant from the centrifugation to the ethanol and mix by inversion. If isopropanol is used, add as much as possible without touching the precipitate.

9. Centrifuge at top speed for 10 min.

10. Pour away supernatant by opening and inverting the tube. The plasmid should be visible as a small white spot in the bottom of the tube.

11. Add 1 mL 70% ethanol. Some protocols specify cold ethanol (-20°C) but ethanol at room temperature works fine.

12. Centrifuge 1 min at top speed.

## Dry plasmid DNA

13. Pour away supernatant by opening and inverting the tube. Be sure to remove as much of the liquid as as possible. If nececessary, spin the tubes a second time ad remove the remaining liquid with a micropipette.

14. Let tubes dry on the bench for 10-15 min with the lid open or at 50°C for 5 min . A [[speedvac]] can also be used if available.

![[alkaline lysis plasmid mini prep_003.png]]

## Reconstitution of plasmid DNA

15. Dissolve pellet in 30-50 µL buffer such as:

| Buffer                                        | Tris-HCl(mM) | EDTA(mM) | pH          |
| --------------------------------------------- | ------------ | -------- | ----------- |
| [[TE]] buffer                                 | 10           | 0.1      | 8           |
| Qiagen EB buffer                              | 10           | -        | 8.5         |
| Qiagen Buffer AE                              | 10           | 0.5      | 9.0         |
| Sigma Genelute Elution Solution               | 10           | 1 mM     | approx. 8.0 |
| NZYMiniprep AE buffer (does not contain EDTA) | ?            | ?        | ?           |

Any resuspension buffer from a commercial plasmid miniprep kit is probably fine for this.

16. Done! Store your DNA in fridge (4-8°C) or freezer (-20°C).


A [[snik-short\|short]] protocol for printing.


## Usage

5 µL of this prep should give a fairly strong band on an agarose gel, 10 µL of this prep can be used for restriction cutting to spot correct clones. This DNA can also be used as template for PCR or to transform E. coli, yeast and probably most other organisms. This DNA prep can be purified using for a clean-up kit (for example Quiagen QIA quick PCR purification columns) prior to cloning.
The DNA is pure enough to digest and use for in-vivo gap repair cloning in S. cerevisiae.

## Notes

This procedure is based on the alkaline lysis procedure described in [Birnboim, H.C., Doly, J., 1979. A rapid alkaline extraction procedure for screening recombinant plasmid DNA. Nucleic Acids Res. 7, 1513–1523.](https://www.ncbi.nlm.nih.gov/pubmed/388356).

The procedure takes advantage of the fact that plasmids are relatively small super coiled DNA
molecules and bacterial chromosomal DNA is much larger and less supercoiled. This difference in topology allows for selective precipitation of the chromosomal DNA and cellular proteins from plasmids and RNA molecules. The cells are lysed under alkaline conditions, which denatures both nucleic acids and proteins, and when the solution is neutralized by the addition of Potassium Acetate, chromosomal DNA and proteins precipitate because it is impossible for them to renature correctly (they are so large). Plasmids renature correctly and stay in solution, effectively separating them from chromosomal DNA and proteins.



## Solutions

### P1

- 50 mM Tris-HCl
- 10 mM EDTA (292,248 g/mol)
- 100 µg/mL RNase A, pH 8.0

Dissolve 6.06 g Tris base (121.14 g/mol) and 3.72 g Na<sub>2</sub>EDTA•2H<sub>2</sub>O (372.2 g/mol) in 800 mL water.
Adjust to pH 8.0 with concentrated HCl (use protection!).

Add 100 µl of RNase (20 mg/ml) to 20 mL of P1.
This solution can be stored at 4°C for long periods.
RNase is not strictly necessary, but removes RNA from the plasmid prep.
When the cells are lysed in the next step, the RNase will catalyze hydrolysis of all RNA molecules into nucleotides, but the DNA will not be damaged.

### P2

- 1% SDS
- 0.2 M NaOH (39,99711 g/mol)

Dissolve 8 g NaOH in 950 mL water.
Add 50 mL of a 20% (w/v) [[SDS]] water solution.

SDS is an ionic detergent which disrupts cell membranes and destabilizes all hydrophobic interactions holding various macromolecules
in their native conformation. The high pH of the 0.2 M NaOH also denatures macromolecules by changing the condition of ionizable groups
(ionizing certain groups and deionizing others).

The clearing you should see is because the cells are lysing.
The viscosity of the solution is increased by the increase in concentration of macromolecules in solution (a result of the cell lysis).

### P3

- 3.0 M Potassium Acetate (KCH3COO; 98,14 g/mol), pH 5.5

There are two ways to prepare this solution.

Glacial or anhydrous acetic acid is essentially water free acetic acid.
It has a density of 1.05 g/mL.
For one liter, add 3 * 60.05 = 180.15 g glacial acetic acid in a 1 L beaker.
Add water to about 500 mL.
Add KOH pellets until pH is 5.5.
Be careful not to overshoot the pH, it may be safe to use a 3M KOH solution just before the right pH.

Alternatively, dissolve 294.5 g potassium acetate powder in 500 mL water.
Adjust the pH with glacial acetic acid (~110 mL was needed when this was attempted).
Add water to one liter.

This is probably the key step in the alkaline lysis procedure. The low pH of the Potassium acetate solution
neutralizes the NaOH and when the pH returns to near-neutrality then the macromolecules renature.
The proteins and large DNA molecules do not renature correctly however. They form hydrophobic, ionic and hydrogen
bonds with each other non-specifically because the correct conformation of the molecule was not maintained during denaturation.
The plasmid DNA molecules, however, never really fully denatured because they are small circular molecules, which are supercoiled.
Even though the hydrogen bonds between base pairs were broken by the high pH, they reform correctly when the pH is lowered.
The large DNA molecules (chromosomal DNA) and proteins form precipitates because they bind to each other in a large
aggregate but the plasmids don't precipitate because they renature correctly and don't become part of the large multi-molecule aggregates.
Thus plasmid DNA remains in solution while proteins and other DNA molecules precipitate.

### TE-buffer

[[TE]]

### Further reading

- [The Basics: How Alkaline Lysis Works](https://bitesizebio.com/180/the-basics-how-alkaline-lysis-works)
- [How to Identify Supercoils, Nicks and Circles in Plasmid Preps](https://bitesizebio.com/13524/how-to-identify-supercoils-nicks-and-circles-in-plasmid-preps)
- [Plasmid vs. Genomic DNA Extraction: The Difference](https://bitesizebio.com/1660/plasmid-v-genomic-dna-extractionthe-difference)
- [Alkaline lysis - Wikipedia](https://en.wikipedia.org/wiki/Alkaline_lysis)

- [![](http://img.youtube.com/vi/8xEDEJ0DHFA/0.jpg)](http://www.youtube.com/watch?v=8xEDEJ0DHFA "Isolating_Plasmid_DNA.png")
- [![](http://img.youtube.com/vi/pw5jgvKn6dw/0.jpg)](http://www.youtube.com/watch?v=pw5jgvKn6dw "Isolating_Plasmid_DNA.png")



### Lista de materiais em Português

2-3 dias antes da aula:

- LB com ampicilina (100 µg/mL) ~ 25-50 mL
- 10 Tubos 2 mL

No dia da aula:

- Tips amarelas (novos!)
- Tips azuis (novos!)
- 12 tubos Eppendorf com 1 mL tampão P1 (marcados "P1")
- 12 tubos Eppendorf com 1 mL tampão P2 (--"--    "P2")
- 12 tubos Eppendorf com 1 mL tampão P3 (--"--    "P3")
- 12 tubos com 1 mL TE x1
- 4 tubos Falcon 50 mL (usados)
- 4 suportes para tubos Eppendorf
- 4 suportes para tubos Falcon 50 mL
- 4 tubos Falcon 50 mL com 25-50 mL EtOH 96-100% (etanol absoluto para DNA/RNA)
- 4 tubos Falcon 50 mL com 25-50 mL EtOH 70% (v/v) (Feito com agua ultrapura)
- 4 copos com Tubos eppendorf 1.5 mL (novos, mas não necessariamente estéreis)
- microcentrifuga
- Agarose para geis
- Tampão TAE x1
- Tampão TAE stock
- 4 copos de 50-100 mL
- 1 proveta 50-100 mL
- 4 erlenmeyers 250 mL
- 2 tinas de eletroforese
- Fonte de eletricidade
- Barquinhos de pesagem (plástico)






### Notes



CAVAN plasmid miniprep: This procedure is based on the alkaline lysis procedure developed by Birnboim and Doly (Nucleic Acids Research 7:1513, 1979).


Procedure:

- Inoculate 1 colony in 3 ml LB+amp; O/N 37°C shaking
- Put cell suspension in 2 mL tube
- Spin down at 14000 RPM for 30s
- Resuspend with 300µl Resuspension solution (vortex)
- Add 300 µl Lysis solution and invert 3X (do NOT vortex)
- Incubate up to 5 minutes (not longer!)
- Add 300µl Neutralization solution and invert 3X (do NOT vortex)
- Incubate up to 5 minutes
- Spin down for 10 min at 14000 RPM at 4°C
- Pipet the supernatant in a new epp
- Add 750µl of Isopropanol (precipitation)
- Vortex and incubate 2 min at RT
- Spin down at 4°C for 15 min (14000 RPM)
- Discard supernatan
- Wash pellet with 300 µl of 70% EtOH
- Spin down at 4°C for 5 min at 14000RPM
- Discard supernatan
- Repeat washing step
- Dry pellet with speedvac for 30 min (or overnight to the air)
- Add 50 µl of TE-buffer
(no guanidine hydrochloride to permanently inactivate nucleases in nuclease rich species)

Solutions:
Resuspension solution: 50 mM Tris-HCl (121,14 g/mol), 10 mM EDTA (292,248 g/mol), 100 µg/mL RNase A, pH 8.0
Stock solution:
1L: 6,057 g Tris + 3,722 g EDTA.2H2O ; adjust to pH 8,0 (HCl)
500 mL: 3,0285 g Tris + 1,861 g EDTA.2H2O ; adjust to pH 8,0 (HCl)

Working solution:
Add 0,6 ml of RNase (20 mg/ml) to 100 ml of resuspension solution store at 4°C

When the cells are lysed in the next step, the RNase will catalyze hydrolysis of all RNA molecules into nucleotides, but the DNA will not be affected.

Lysis solution: 1% SDS; 0,2 M NaOH (39,99711 g/mol)
1L: 8,0 g NaOH pellets in 900 ml MQ-water; autoclave; add 100 ml of SDS 10%
500 mL: 4,0 g NaOH pellets in 450 ml MQ-water; autoclave; add 50 ml of SDS 10%

SDS is an ionic detergent which disrupts cell membranes and destabilizes all hydrophobic interactions holding
various macromolecules in their native conformation. The high pH of the 0.2 M NaOH also denatures macromolecules by
changing the condition of ionizable groups (ionizing certain groups and deionizing others).
The clearing you see is because the cells are lysing. The viscosity of the solution is increased by the increase
in concentration of macromolecules in solution (a result of the cell lysis).

Neutralisation solution: 3.0 M Potassium Acetate (KCH3COO; 98,14 g/mol), pH 5.5
1L: 294,45 g KAc in 500 ml H2O; pH to 5,5 with acetic acid (CH3COOH); H2O to 1L
500 mL: 147,225 g KAc in 250 ml H2O; pH to 5,5 with acetic acid, H2O to 500 mL

This is really the key step in the alkaline lysis procedure. The low pH of the Potassium acetate solution neutralizes
the NaOH and when the pH returns to near-neutrality then the macromolules renature. The proteins and large DNA molecules
do not renature correctly however. They form hydrophobic, ionic and hydrogen bonds with each other nonspecifically because
the correct conformation of the molecule was not maintained during denaturation. The plasmid DNA molecules, however, never really
fully denatured because they are small circular molecules, which are supercoiled. Even though the hydrogen bonds between base pairs
were broken by the high pH, they reform correctly when the pH is lowered. The large DNA molecules (chromosomal DNA) and proteins form
precipitates because they bind to each other in a large aggregate but the plasmids don't precipitate because they renature correctly
and don't become part of the large multi-molecule aggregates. Thus plasmid DNA remains in solution while proteins and other DNA molecules precipitate.

TE-buffer (1X): 1mM EDTA (292,248 g/mol), 10 mM Tris (121,14 g/mol); HCl pH 8.0
  	1L (10X): 3,722 g EDTA .2H2O  ;  12,114 g Tris
 	100 mL (10X): 0,3722 g EDTA .2H2O  ;  1,2114 g Tris

TE buffer is commonly used to redissolve DNA because it contains EDTA. The EDTA will chelate magnesium ions, which are a
cofactor for most nucleases (enzymes which degrade nucleic acids). If your DNA prep becomes contaminated with a nuclease
(like the ones produced by the cells in your skin) then the nuclease will be inactivated by the fact that the magnesium cofactor
is unavailable in the solution (because it is chelated by the EDTA).
